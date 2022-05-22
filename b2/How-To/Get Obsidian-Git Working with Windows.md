## What is the problem?
Obsidian-Git requires a careful orchestration of Git settings, otherwise it fails to auto-push commits, especially if one is using SSH-based authentication with a passphrase applied to the private key.

The error keeps coming: `permission denied (publickey). Make sure you have correct access rights and the repository exists.`

The problem is with the passphrase. When you push something from the command line, you have to enter the passphrase at the prompt. This step obviously doesn't happen in the background push done by Obsidian-Git plugin. Hence