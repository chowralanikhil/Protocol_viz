# AI usage log

**Platform:** OpenAI Codex desktop agent  
**Model:** GPT-5.6 (Codex agent)

## Prompt history / artifacts

| Stage | Prompt or request | Result used |
|---|---|---|
| Requirements | “Prepare” the supplied Application Layer Dashboard assignment. | Parsed the brief and identified the required two-panel UI, three activities, accurate simulated protocols, controls, AI evidence, and reflection. |
| Architecture | Create a self-contained dashboard that needs no server setup. | Chose an HTML/CSS/JavaScript implementation so the submission can run by opening one file. |
| UI generation | Build exactly two responsive panels, with activity controls on the left and a protocol sequence on the right. | Produced the dual-panel layout and mobile stacking behavior. |
| Protocol modelling | Model accurate DNS/HTTP, SMTP, and streaming HTTP message sequences. | Added DNS A/MX messages; HTTP request/status/header examples; SMTP command-response conversation; HLS manifest/playlist and segment exchanges. |
| Iteration | Ensure every activity starts the visualizer immediately and it can pause, step, and replay. | Added synchronized activity handlers plus previous, next, pause/resume, and replay controls. |

## Human review and corrections

The generated design was reviewed against the assignment brief. The mail flow includes a DNS **MX** lookup rather than an A lookup because the destination mail exchanger is discovered through MX records. The streaming flow uses an HLS master manifest, variant playlist, and repeated media segment HTTP GETs, rather than representing a stream as one indefinite HTTP response. These corrections keep the simulation aligned with common application-layer behavior.

This file, together with the Codex task conversation, is retained as evidence of AI-assisted development.
