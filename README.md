# blockchain
Hyper-ledger Fabric blockhain mutipeer setup instructions


Install Pre-requisites
https://hyperledger.github.io/composer/installing/installing-prereqs.html


On the central host:
curl -O https://github.com/lalbsah/blockchain/raw/master/Central.zip

On The peer node:
curl -O https://github.com/lalbsah/blockchain/raw/master/Peer2.zip


Change needed on the peer node:
1. docker-composer-Peer2.yml - Replace the IP address with your central host IP
extra_hosts:
 - "orderer.example.come:<Central HOST IP>”

2. Replace the central host IP under channel creation command. 
# Create the channel
docker exec peer2.org1.example.com peer channel fetch config -o <Central HOST IP> -c composerchannel

3. start-fabric-Peer2.sh
