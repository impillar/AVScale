# App Transformations in AVScale

## code: The main code for transforming an Android apps
+ ./backdoor.py:   Merge two apps into one
+ ./dynamic.py:    Make the malware as payload and be downloaded and executed during runtime
+ ./fusion.py:     Merge two apps in batch, by invoking the APIs in backdoor.py
+ ./packer.py:     Pack one app with the Bangcle
+ ./preprune.py:   Cluster classes of one apps based on control flow or data flow relationship
+ ./prune.py:		Coarse-grained pruning by only removing functional code in methods
+ ./prune_deeper.py:	Fine-grained pruning by removing specific modules in one app
+ ./resigning.py:		Resign one app with self-certificate
+ ./resigning_mykey.py: Resign one app with the AOSP key
+ ./unsigning.py:		Remove the certificate of one app
  
 ## data: The generated apps after transformations and their original
 +./dynamic.csv:    "ORI_APP", "INDIRECT_APP" and "DIRECT_APP" are the original apps, apps with payloads, and payload apps, respectively.
 +./dynamic_capability.csv:  "ORI_APP", "SMS", "SCREEN", ... are the original apps, and apps with their malicious code executed by SMS broadcast receivers, screen receivers, present receivers, ...., respectively
 + ./fusion.csv:     "APP1", "APP2" and "FUSED_APP" are the two merged apps and the final app, respectively
 + ./packer.csv:     The fist column shows the hashcode of the original apps, and the second shows the packed apps' hashcode
 + ./prune.csv:		 "ORI_APP", "PRUNE_SMALI", "PRUNE_NATIVE" and "PRUNE_XML" are the original apps, apps without smali, apps without native, apps without xml
 + ./resig_aosp.csv: "ORI_APP", "RE-SIGN_AOSP" are the original apps and resigned apps with AOSP keys
 + ./resign_mykey.csv: "ORI_APP", "RE-SIGN_SELF_KEY" are the original apps and resigned apps with self keys
 + ./unsign.csv:		"ORI_APP", "UNSIGN" are the original apps and unsigned apps