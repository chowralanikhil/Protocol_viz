# AI usage log

**Platform:** OpenAI Codex desktop agent  
**Model:** GPT-5.6 Codex agent

## Assignment 1 work

| Stage | Request | Result used |
| --- | --- | --- |
| Requirements | Prepare the Application Layer Dashboard assignment. | Identified the required two-panel UI, three activities, application-layer protocol simulations, controls, evidence, and reflection. |
| Interface | Build a self-contained dashboard. | Implemented a responsive HTML/CSS/JavaScript application with exactly two main panels. |
| Protocol modelling | Model DNS/HTTP, SMTP, and HTTP streaming. | Added DNS A/MX examples, HTTP request/response headers, SMTP dialogue, and HLS manifest/segment exchanges. |

## Assignment 2 extension

| Stage | Request | Result used |
| --- | --- | --- |
| Requirements review | Update the same project using Assignment 2. | Read the brief and retained the left Activity panel while extending the right panel with two synchronized layer views. |
| Architecture | Keep Application and Transport views synchronized. | Used one shared playback position; both timelines load on the same activity action and the active position is mapped into either tab. |
| TCP modelling | Add accurate TCP state, flags, Seq/Ack fields, windows, data delivery, and teardown. | Added `SYN`, `SYN, ACK`, `ACK`, `PSH, ACK`, and `FIN, ACK` events, monotonically advancing sequence/acknowledgement values, advertised receive windows, data lengths, and connection-close exchanges. |
| Review | Check protocol correctness. | Corrected the design to account for SYN consuming one sequence number, data consuming its displayed length, ACK values acknowledging the next expected byte, and FIN consuming one sequence number. |

## Human review and corrections

For mail, DNS uses an **MX** lookup because mail routing discovers a mail exchanger, not merely a web-host A record. For streaming, the browser obtains a master manifest, a quality playlist, and separate media segments; it is not one indefinite HTTP download.

The TCP view is deliberately a simulation, but it follows the reliable byte-stream model: the 3-way handshake completes before application data, `PSH, ACK` segments carry ordered data, acknowledgement numbers indicate the next expected byte, advertised windows provide receive-flow-control context, and a four-segment FIN/ACK close follows the exchange. The congestion-window label is explanatory only; it does not claim to implement a real congestion-control algorithm.

This log and the Codex task conversation are retained as evidence of AI-assisted development.
