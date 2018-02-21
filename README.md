# blockchain
Hyper-ledger Fabric blockhain mutipeer setup instructions


Install Pre-requisites
https://hyperledger.github.io/composer/installing/installing-prereqs.html


On the central host:
1. Download https://github.com/lalbsah/blockchain/raw/master/Central.zip
2. Unzip Central.zip
3. Go to Central/fabric-dev-servers directory
4. Run startFabric.sh

On The peer node:
1. Download https://github.com/lalbsah/blockchain/raw/master/Peer2.zip
2. Unzip Peer2.zip
3. Go to Peer2/fabric-dev-servers/composer directory to make some changes to docker-composer-Peer2.yml and replace the IP address with your central host IP
extra_hosts:
 \- "orderer.example.come:{Central HOST IP}”

4. Go to Peer2/fabric-dev-servers directory and replace the central host IP under channel creation command. 
# Create the channel
docker exec peer2.org1.example.com peer channel fetch config -o {Central HOST IP} -c composerchannel

5. start-fabric-Peer2.sh
