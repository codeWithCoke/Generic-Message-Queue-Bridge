# Generic-Message-Queue-Bridge
A generic bridge to relay messages between different MQs fast and safe
## Guarantee
This bridge emphasises speed and message safety. Message ordering is not always guaranteed but in a best-effort manner.
## Core Flow
```mermaid
flowchart LR
    A((Start)) --> B["Subscriber receives message from MQ'"]
    B --> C["Publish message to MQ&quot; - no ack to MQ' yet"]
    C --> D["Wait for ack from MQ&quot;"]
    D --> E["Upon ack from MQ&quot;, acknowledge message in MQ'"]
    E --> F((Next Message))
```
# This Repo is under development. Please message if you have specific broker technology that you want to be supported.
