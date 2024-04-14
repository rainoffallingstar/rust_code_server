### rust_code_server

A code server docker container with rustc pre-install, based on vscode-web container.

#### how to use
install
```
docker pull fallingstar10/rustcodesever:latest
```
start a container,the default user and $HOME is "coder"
```
docker run -it -p 8989:8080 -e PASSWORD=***********  --name rust-code-web fallingstar10/rustcodesever:latest
```
