# 하이퍼레저 2.0 구성 (Ubuntu 18.04)

1. Building Your First Network:박진환, 이영준(7/27:5시)
https://hyperledger-fabric.readthedocs.io/en/latest/build_network.html
2. Writing Your First Application:최규남,유학용(8/3:5시)
3. Commercial paper tutorial:전부현(8/10:5시)
4. 오프 세미나 : 8/17(오후 13시 ~ 17시) 장소 : KISA 회의실


1. sudo apt update
2. sudo apt install curl
3. sudo apt install docker.io
4. sudo usermod -aG docker $USER
5. su $USER
6. sudo apt install docker-compose
7. wget https://dl.google.com/go/go1.12.7.linux-amd64.tar.gz
8. tar xvf go1.12.7.linux-amd64.tar.gz 
9. sudo cp -r go /usr/local
10.curl -sSL http://bit.ly/2ysbOFE | bash -s -- 2.0.0-alpha 2.0.0-alpha 0.4.15
11.vi ~/.bashrc 맨 아래에 아래 명령어 추가
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin:$HOME/fabric-samples/bin

12. source ~/.bashrc
13. go version
14. cryptogen --help
15. cd fabric-samples/first-network/
16.  ./byfn.sh up
