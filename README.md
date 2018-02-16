# blockchain
Hyper-ledger Fabric blockhain 


Change needed on Host2(Peer2):
1. docker-composer-Peer2.yml - Replace the IP address with your host1 IP
extra_hosts:
 - "orderer.example.come:192.168.1.151"

2. Replace the host 1 IP under channel creation command. 
3. start-fabric-Peer2.sh

