vAuth Vault Agent Helper
=======

The vAuth Vault Agent helper application for automatically generating HashiCorp Vault AppRole credential files using credentials fetched from vAuth.

# Getting Started

1. Download the latest release of the vault-agent-vauth-helper from the Github releases.

2. Create a `config.hcl` configuration file in the directory where the `vault-agent-vauth-helper` binary exists

```
sync_interval       = 10
role_id_file_path   = "/tmp/role.txt"
secret_id_file_path = "/tmp/secret.txt"
```

|Setting|Description|
|--|--|
|sync_interval|The interval at which the agent will check for updates to the role ID and secret ID|
|role_id_file_path|The path on the system where the approle role ID will be written|
|secret_id_file_path|The path on the file system where the approle secret ID will be written|

3. Run the `vauth-agent` executable on the target system