# nexus-prover

run nexus prover on cli

install packages:

```
apt update && apt install -y pkg-config libssl-dev
apt update && apt install -y build-essential clang
```

install protoc compiler:

```
sudo apt update
sudo apt install -y protobuf-compiler
```

remove old protoc:

```
sudo rm -rf /usr/local/bin/protoc
sudo rm -rf /usr/local/include/google
sudo rm -rf /usr/bin/protoc
sudo apt remove -y protobuf-compiler
```

reinstall it:

```
PROTOC_VERSION=24.4
wget https://github.com/protocolbuffers/protobuf/releases/download/v${PROTOC_VERSION}/protoc-${PROTOC_VERSION}-linux-x86_64.zip
unzip protoc-${PROTOC_VERSION}-linux-x86_64.zip -d $HOME/.local
export PATH="$HOME/.local/bin:$PATH"
```

run the script:

```
screen -S nexus

curl https://cli.nexus.xyz/ | sh
```

steps:

1. connect your wallet at https://app.nexus.xyz

2. accept the terms and conditions

3. select the 2nd option "start earning NEX by connecting adding your NODE ID"

4. go to dashboard -> add CLI NODE and get the node code and paste it in the terminal

5. if the proving started detach the session:

```
ctrl+a+d
```
