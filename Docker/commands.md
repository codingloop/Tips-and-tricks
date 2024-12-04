## 1. **Inspecting**
- **View file system**
```
docker system df
```

## 2. **Cleanup**
### 1. Cleanup resources in bulk
- Remove Stopped Containers
```
docker container prune
```

- Remove Unused Images
```
docker image prune
```

- For all unused images (not just dangling):
```
docker image prune -a
```

- Remove Unused Volumes
```
docker volume prune
```

- Remove Unused Networks
```
docker network prune
```

### 2. Cleanup specific resource
- Remove a Specific Container
```
docker rm <container_id>
```

- Remove a Specific Image
```
docker rmi <image_id>
```

- Remove a Specific Volume
```
docker volume rm <volume_name>
```

### 3. Remove all at once
```
docker system prune
```
This removes:
- Stopped containers
- Unused networks
- Dangling images (images not associated with any container)
- Build cache

Add `-a` to also remove unused images (not just dangling):
```
docker system prune -a
```

By default, docker system prune does not remove unused volumes. Use the --volumes flag to include them:
```
docker system prune -a --volumes
```

