geth --datadir node init genesis.json

geth --datadir node --ipcpath "~/Library/Ethereum/geth.ipc"

geth --datadir node --nodiscover --ipcpath "~/Library/Ethereum/geth.ipc"

# ipc 연결
geth attach ~/Library/Ethereum/geth.ipc

# minor를 쓰기 위해선 계정이 필요함

personal.newAccount()
1234
1235

eth.accounts

eth.coinbase

# 계정 변환
miner.setEtherbase(eth.accounts[1])

miner.start(8)

miner.stop()

# 밸런스 확인
web3.fromWei(eth.getBalance(eth.coinbase),'ether')

# 다른사람한테 연결

admin.nodeInfo.enode

admin.addPeer("enode://338582013a1d9c5cf3d04f21dfa6d1e824fa8d756c70645af07d1e37ee37c9cf07c53302cce84efa24ac72219f21affc386502d31871eb5e4d7adb13334a3fd4@127.0.0.1:30303?discport=0")

net.peerCount