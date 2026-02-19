```mermaid
flowchart LR

subgraph C[Browser Client]
  UI[Timeline UI and Voice UI]
  SM[State Summary Builder]
  CE[Command Executor]
  PS[(Project State Store)]
  AE[Audio Engine WebAudio plus WASM]
  AM[Asset Manager]
  MIC((Mic Input))

  UI --> SM
  UI --> CE
  CE <--> PS
  PS --> UI
  CE --> AE
  AM <--> AE
  UI <--> AM
  MIC --> UI
end

subgraph S[Backend AI Services]
  ASR[ASR Service]
  AG[Agent Service]
  HUM[Hum to MIDI Service]
  SYN[SynthGen Service]
end

UI --> ASR
ASR --> AG
AG --> UI

UI --> HUM
HUM --> UI

UI --> SYN
SYN --> UI
```

