## 1. Node js starting error
nodejs: listen EACCES: permission denied 0.0.0.0:80

### Fix:
1. Open a admin cmd
2. Execute below commands
    - `net stop winnat`
    - `net start winnat`

## 2. DockerDesktop not clearing diskspace even after pruning
### Fix:
1. Open admin powershell
2. Execute below command
   ```
   Optimize-VHD -Path "/path/to/file/docker_data.vhdx" -Mode Full
   ```
   Path can be found in **DockerDesktop/Settings/Resources/**
