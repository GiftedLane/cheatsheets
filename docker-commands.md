### Docker Commands

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
