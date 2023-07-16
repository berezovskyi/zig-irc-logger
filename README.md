## Getting started

```sh
cp docker-compose.yml.sample docker-compose.yml
mkdir data/ 
(cd data/ && git clone git@github.com:berezovskyi/zig-irc-logs.git repo && cd repo && git checkout live)
ssh-keygen -f secrets/id_ed25519 -t ed25519
ssh-keyscan -t ed25519 github.com > secrets/known_hosts
# for debug builds on macOS
# zig build -Dtarget=x86_64-linux
docker-compose up --build
# make the .ssh volume :ro
docker-compose up -d --build
```