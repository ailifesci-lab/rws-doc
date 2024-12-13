```bash
docker run -it \
	--name='dev-node-qpod-pages' \
	--hostname='QPod-node' \
	-p 3000:3000 \
	-v $(pwd):/root/project-docs \
	-w /root/project-docs \
	qpod/node

docker exec -it dev-node-qpod-pages bash

cd rws-doc

pnpm run install

pmpm run start
```
