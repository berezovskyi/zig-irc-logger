## Getting started

```sh
cp docker-compose.yml.sample docker-compose.yml
mkdir data/ 
(cd data/ && git clone git@github.com:berezovskyi/zig-irc-logs.git repo)
ssh-keygen -f secrets/id_ed25519 -t ed25519
zig build -Dtarget=x86_64-linux && docker-compose up
```