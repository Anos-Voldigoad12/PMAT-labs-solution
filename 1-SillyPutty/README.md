# Challenge 1: SillyPutty
[Link](https://github.com/HuskyHacks/PMAT-labs/tree/main/labs/1-3.Challenge-SillyPutty)

## Basic Static Analysis
1. What is the SHA256 hash of the sample?


2. What architecture is this binary?


3. Are there any results from submitting the SHA256 hash to VirusTotal?


4. Describe the results of pulling the strings from this binary. Record and describe any strings that are potentially interesting. Can any interesting information be extracted from the strings?


5. Describe the results of inspecting the IAT for this binary. Are there any imports worth noting?


6. Is it likely that this binary is packed?

## Basic Dynamic Analysis

1. Describe initial detonation. Are there any notable occurrences at first detonation? Without internet simulation? With internet simulation?


2. From the host-based indicators perspective, what is the main payload that is initiated at detonation? What tool can you use to identify this?


3. What is the DNS record that is queried at detonation?


4. What is the callback port number at detonation?


5. What is the callback protocol at detonation?


6. How can you use host-based telemetry to identify the DNS record, port, and protocol?


7. Attempt to get the binary to initiate a shell on the localhost. Does a shell spawn? What is needed for a shell to spawn?

