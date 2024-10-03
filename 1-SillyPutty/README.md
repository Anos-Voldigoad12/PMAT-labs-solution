# Challenge 1: SillyPutty
[Link](https://github.com/HuskyHacks/PMAT-labs/tree/main/labs/1-3.Challenge-SillyPutty)

## Basic Static Analysis
1. What is the SHA256 hash of the sample?
```
    0c82e654c09c8fd9fdf4899718efa37670974c9eec5a8fc18a167f93cea6ee83
```

2. What architecture is this binary?
```
    Portable Executable 32
```

3. Are there any results from submitting the SHA256 hash to VirusTotal?

![VirusTotal Results](https://github.com/user-attachments/assets/04f3f7bc-fa5d-46ec-ac24-54950d0d7aba)


4. Describe the results of pulling the strings from this binary. Record and describe any strings that are potentially interesting. Can any interesting information be extracted from the strings?
```
    		SSHCONNECTION@putty.projects.tartarus.org-2.0-
		%s Security Alert
		The first %s supported by the server
		is %s, which is below the configured
		warning threshold.
		Do you want to continue with this connection?
		%s Security Alert
		The first host key type we have stored for this server
		is %s, which is below the configured warning threshold.
		The server also provides the following types of host key
		above the threshold, which we do not have stored:
		Do you want to continue with this connection?
		%s Key File Warning
		You are loading an SSH-2 private key which has an
		old version of the file format. This means your key
		file is not fully tamperproof. Future versions of
		%s may stop supporting this private key format,
		so we recommend you convert your key to the new
		You can perform this conversion by loading the key
		into PuTTYgen and then saving it again.
		The session log file "%.*s" already exists.
		You can overwrite it with a new session log,
		append your session log to the end of it,
		or disable session logging for this session.
		Hit Yes to wipe the file, No to append to it,
		or Cancel to disable logging.	
```

5. Describe the results of inspecting the IAT for this binary. Are there any imports worth noting?

![image](https://github.com/user-attachments/assets/85cce69b-364d-4375-80ea-879f346e1f34)


6. Is it likely that this binary is packed?
```
	Yes, because the virtual-size is much greater than the raw-size
```
![image](https://github.com/user-attachments/assets/a13ee614-a812-482f-b513-5270303582ce)


## Basic Dynamic Analysis

1. Describe initial detonation. Are there any notable occurrences at first detonation? Without internet simulation? With internet simulation?


2. From the host-based indicators perspective, what is the main payload that is initiated at detonation? What tool can you use to identify this?


3. What is the DNS record that is queried at detonation?


4. What is the callback port number at detonation?


5. What is the callback protocol at detonation?


6. How can you use host-based telemetry to identify the DNS record, port, and protocol?


7. Attempt to get the binary to initiate a shell on the localhost. Does a shell spawn? What is needed for a shell to spawn?

