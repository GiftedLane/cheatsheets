### Docker Commands

```bash
# LIST all the Docker containers on your system
docker ps -a
```
```bash
# STOP specific Docker containers
docker stop [container_id or container_name]
```
```bash
# STOP ALL Docker containers
docker stop $(docker ps -q)
```
```bash
# DELETE the container
docker rm [container_id or container_name]
```
```bash
# DELETE all Docker containers
docker rm $(docker ps -a -q)
```
```bash
# DELETE all stopped Docker containers
docker container prune
```
```bash
# FORCE DELETE all stopped Docker containers
docker container prune -f
```
```bash
# list all images
docker images -a
```
```bash
# delete images
docker rmi Image Image
```
```bash
# list dangling images that have no relationship to any tagged images
docker images -f dangling=true
```
```bash
# DELETE dangling images that have no relationship to any tagged images
docker image prune
```
