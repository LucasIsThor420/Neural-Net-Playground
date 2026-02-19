```mermaid
flowchart LR
  UI[Browser] --> ORCH[AI Orchestrator API]
  ORCH --> ASR[ASR module]
  ORCH --> CMD[Command Agent module]
  ORCH --> HUM[Hum to MIDI module]
  ORCH --> SYN[Synth Preset Gen module]
  ORCH --> STORE[(Assets and Logs)]
  ORCH --> UI
```
