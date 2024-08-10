#### 1. Check space usage
`du -h --max-depth=0 /root/directory`

#### 2. Create link file in linux
`ln -s /source/file /destination/file2`

Above command will create file2 link which is pointing to file


#### 3. Uninstall application completely from linux
`apt-get remove --purge packagename` => Removes the package and delete the files associated

`apt-get autoremove --purge` => Removes the orphaned packages and deletes the files
