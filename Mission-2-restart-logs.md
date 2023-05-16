# Restart your validator three times during Mission 2

## Valoper
```humanvaloper13gq2yj4486w3ajvafgxj7tzqn7w0v7njynyszt```

## Restart 1
```
May 16 13:00:20 staketab humansd[28671]: 1:00PM INF indexed block exents height=71607 module=txindex server=node
May 16 13:00:24 staketab humansd[28671]: 1:00PM INF Timed out dur=4376.14923 height=71608 module=consensus round=0 server=node step=1
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF received proposal module=consensus proposal={"Type":32,"block_id":{"hash":"E2B2C3761AE1932B0C2D9A301F90DCF96782D88EBBD1B735E7A4BB3DE365D9BC","parts":{"hash":"424093D7A396777FC455A64597DEA2EA3D1DDA3EFD50FA16DEC190A5EFC46AA7","total":1}},"height":71608,"pol_round":-1,"round":0,"signature":"cOQoae+2CJW+927ytUQSJBiVGGJ5iSIYqGvbUMuFAdo6xDENvpmCAljSdCmoPnigCQ0O1r/t5+swEXpeK8DXBA==","timestamp":"2023-05-16T11:00:24.942866059Z"} server=node
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF received complete proposal block hash=E2B2C3761AE1932B0C2D9A301F90DCF96782D88EBBD1B735E7A4BB3DE365D9BC height=71608 module=consensus server=node
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF finalizing commit of block hash={} height=71608 module=consensus num_txs=0 root=B828DCA921328627ADC7436BDEC04DA1BE57E8739E683FF72097D4F492D1D8A2 server=node
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF executed block height=71608 module=state num_invalid_txs=0 num_valid_txs=0 server=node
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF commit synced commit=436F6D6D697449447B5B3133312031353920313335203130382031323320323233203133302038372032303820393020313237203130352036352031333420313620313639203133352038322031363020323136203134382036342031303220323039203234362032333220323438203136203235352032352031393220305D3A31313742387D
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF committed state app_hash=839F876C7BDF8257D05A7F69418610A98752A0D8944066D1F6E8F810FF19C000 height=71608 module=state num_txs=0 server=node
May 16 13:00:25 staketab humansd[28671]: 1:00PM INF indexed block exents height=71608 module=txindex server=node
^C
#### sudo systemctl restart humansd && sudo journalctl -u humansd -f
-- Logs begin at Sun 2023-05-14 06:31:44 CEST. --
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=statesync msg={} server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=pex msg={} server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF service stop book=/root/.humansd/config/addrbook.json impl={"Logger":{}} module=p2p msg={} server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM ERR Stopped accept routine, as transport is closed module=p2p numPeers=0 server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF Closing rpc listener listener={"Listener":{}} server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF Saving AddrBook to file book=/root/.humansd/config/addrbook.json module=p2p server=node size=119
May 16 13:00:31 staketab humansd[28671]: 1:00PM INF RPC HTTP server stopped err="accept tcp [::]:26657: use of closed network connection" module=rpc-server server=node
May 16 13:00:31 staketab humansd[28671]: 1:00PM ERR Error serving server err="accept tcp [::]:26657: use of closed network connection" server=node
May 16 13:00:31 staketab systemd[1]: Stopped humansd Node Service.
May 16 13:00:31 staketab systemd[1]: Started humansd Node Service.
May 16 13:00:31 staketab humansd[31284]: 1:00PM INF Unlocking keyring
May 16 13:00:31 staketab humansd[31284]: 1:00PM INF starting ABCI with Tendermint
May 16 13:00:32 staketab humansd[31284]: 1:00PM INF starting node with ABCI Tendermint in-process
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start impl=EventBus module=events msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF ABCI Handshake App Info hash="���l{߂W�Z\x7fiA�\x10��R�@f����\x10�\x19�\x00" height=71608 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF ABCI Replay Blocks appHeight=71608 module=consensus server=node stateHeight=71608 storeHeight=71608
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Completed ABCI Handshake - CometBFT and App are synced appHash="���l{߂W�Z\x7fiA�\x10��R�@f����\x10�\x19�\x00" appHeight=71608 module=consensus server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF This node is a validator addr=B8C7E45D40944E08CA38CEBE1262C4306A71E985 module=consensus pubKey=Cl+hB8Iyx/UQfY7ey2k0DP+S3/4+pb4uCy2r4wjRT9w= server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF P2P Node ID ID=b1f13e9971cfdcf784fb0efbd1b72417d5410a02 file=/root/.humansd/config/node_key.json module=p2p server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Adding persistent peers addrs=["2631445e3d6b93a5f717f14b27a5b057b88b7d9a@65.108.224.156:28656","0ab5a0c4fd3d85462da5fa149f3eb6d5702a4f32@118.193.37.229:26656","054c81f412213c90e77b295d6061a4a4b34d8f8f@141.95.99.214:14356","ca1e46048e4a9b65d60bc9e749aa431401f34ed7@144.76.45.59:26656","e6489cf86b51fa37cae968ccbbda1da03b742a5e@128.140.56.206:26656","69a6d587d4bd0d9f37404dbc03029c6220bde175@81.30.157.35:19656","b9767aa2312748caaf67425890768d85186b69b1@5.9.87.205:26646"] module=p2p server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Add our address to book addr={"id":"b1f13e9971cfdcf784fb0efbd1b72417d5410a02","ip":"0.0.0.0","port":26656} book=/root/.humansd/config/addrbook.json module=p2p server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF service start impl=Node msg={} server=node
May 16 13:00:33 staketab humansd[31284]: 1:00PM INF Starting pprof server laddr=localhost:6060 server=node
```

## Restart 2
```
May 16 13:08:43 staketab humansd[31284]: 1:08PM INF executed block height=71694 module=state num_invalid_txs=0 num_valid_txs=0 server=node
May 16 13:08:43 staketab humansd[31284]: 1:08PM INF commit synced commit=436F6D6D697449447B5B3339203730203137372031313020313837203137302033362031393520323431203139322037302031363220313830203132352032303720323132203620323238203139203138332033312031363720323039203233382035312037332031373820323037203130372032333720313830203135385D3A31313830457D
May 16 13:08:43 staketab humansd[31284]: 1:08PM INF committed state app_hash=2746B16EBBAA24C3F1C046A2B47DCFD406E413B71FA7D1EE3349B2CF6BEDB49E height=71694 module=state num_txs=0 server=node
May 16 13:08:43 staketab humansd[31284]: 1:08PM INF indexed block exents height=71694 module=txindex server=node
May 16 13:08:48 staketab humansd[31284]: 1:08PM INF Timed out dur=4919.221393 height=71695 module=consensus round=0 server=node step=1
^C
#### sudo systemctl restart humansd && sudo journalctl -u humansd -f
-- Logs begin at Sun 2023-05-14 06:31:44 CEST. --
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=statesync msg={} server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=pex msg={} server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF service stop book=/root/.humansd/config/addrbook.json impl={"Logger":{}} module=p2p msg={} server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF Closing rpc listener listener={"Listener":{}} server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM ERR Stopped accept routine, as transport is closed module=p2p numPeers=0 server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF Saving AddrBook to file book=/root/.humansd/config/addrbook.json module=p2p server=node size=119
May 16 13:08:51 staketab humansd[31284]: 1:08PM INF RPC HTTP server stopped err="accept tcp [::]:26657: use of closed network connection" module=rpc-server server=node
May 16 13:08:51 staketab humansd[31284]: 1:08PM ERR Error serving server err="accept tcp [::]:26657: use of closed network connection" server=node
May 16 13:08:51 staketab systemd[1]: Stopped humansd Node Service.
May 16 13:08:51 staketab systemd[1]: Started humansd Node Service.
May 16 13:08:51 staketab humansd[1960]: 1:08PM INF Unlocking keyring
May 16 13:08:51 staketab humansd[1960]: 1:08PM INF starting ABCI with Tendermint
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF starting node with ABCI Tendermint in-process
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start impl=EventBus module=events msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF ABCI Handshake App Info hash="������u��i\x11��u(�c\x11�_����\t��3���M" height=71695 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF ABCI Replay Blocks appHeight=71695 module=consensus server=node stateHeight=71695 storeHeight=71695
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Completed ABCI Handshake - CometBFT and App are synced appHash="������u��i\x11��u(�c\x11�_����\t��3���M" appHeight=71695 module=consensus server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF This node is a validator addr=B8C7E45D40944E08CA38CEBE1262C4306A71E985 module=consensus pubKey=Cl+hB8Iyx/UQfY7ey2k0DP+S3/4+pb4uCy2r4wjRT9w= server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF P2P Node ID ID=b1f13e9971cfdcf784fb0efbd1b72417d5410a02 file=/root/.humansd/config/node_key.json module=p2p server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Adding persistent peers addrs=["2631445e3d6b93a5f717f14b27a5b057b88b7d9a@65.108.224.156:28656","0ab5a0c4fd3d85462da5fa149f3eb6d5702a4f32@118.193.37.229:26656","054c81f412213c90e77b295d6061a4a4b34d8f8f@141.95.99.214:14356","ca1e46048e4a9b65d60bc9e749aa431401f34ed7@144.76.45.59:26656","e6489cf86b51fa37cae968ccbbda1da03b742a5e@128.140.56.206:26656","69a6d587d4bd0d9f37404dbc03029c6220bde175@81.30.157.35:19656","b9767aa2312748caaf67425890768d85186b69b1@5.9.87.205:26646"] module=p2p server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Add our address to book addr={"id":"b1f13e9971cfdcf784fb0efbd1b72417d5410a02","ip":"0.0.0.0","port":26656} book=/root/.humansd/config/addrbook.json module=p2p server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF service start impl=Node msg={} server=node
May 16 13:08:53 staketab humansd[1960]: 1:08PM INF Starting pprof server laddr=localhost:6060 server=node
```

## Restart 3
```
May 16 13:12:07 staketab humansd[1960]: 1:12PM INF executed block height=71726 module=state num_invalid_txs=0 num_valid_txs=0 server=node
May 16 13:12:07 staketab humansd[1960]: 1:12PM INF commit synced commit=436F6D6D697449447B5B32343720313333203231382032313720313420373820363920323620323232203536203233322032353220393020313032203134382032343520313431203731203335203634203534203137342032343920313733203139392039302032343520313920323533203139302031333920345D3A31313832457D
May 16 13:12:07 staketab humansd[1960]: 1:12PM INF committed state app_hash=F785DAD90E4E451ADE38E8FC5A6694F58D47234036AEF9ADC75AF513FDBE8B04 height=71726 module=state num_txs=0 server=node
May 16 13:12:07 staketab humansd[1960]: 1:12PM INF indexed block exents height=71726 module=txindex server=node
^C
#### sudo systemctl restart humansd && sudo journalctl -u humansd -f
-- Logs begin at Sun 2023-05-14 06:31:44 CEST. --
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=statesync msg={} server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF service stop impl={"Logger":{},"Switch":{"Logger":{}}} module=pex msg={} server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF service stop book=/root/.humansd/config/addrbook.json impl={"Logger":{}} module=p2p msg={} server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF Closing rpc listener listener={"Listener":{}} server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF Saving AddrBook to file book=/root/.humansd/config/addrbook.json module=p2p server=node size=120
May 16 13:12:13 staketab humansd[1960]: 1:12PM INF RPC HTTP server stopped err="accept tcp [::]:26657: use of closed network connection" module=rpc-server server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM ERR Stopped accept routine, as transport is closed module=p2p numPeers=0 server=node
May 16 13:12:13 staketab humansd[1960]: 1:12PM ERR Error serving server err="accept tcp [::]:26657: use of closed network connection" server=node
May 16 13:12:13 staketab systemd[1]: Stopped humansd Node Service.
May 16 13:12:13 staketab systemd[1]: Started humansd Node Service.
May 16 13:12:13 staketab humansd[3327]: 1:12PM INF Unlocking keyring
May 16 13:12:13 staketab humansd[3327]: 1:12PM INF starting ABCI with Tendermint
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF starting node with ABCI Tendermint in-process
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start impl=multiAppConn module=proxy msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start connection=query impl=localClient module=abci-client msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start connection=snapshot impl=localClient module=abci-client msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start connection=mempool impl=localClient module=abci-client msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start connection=consensus impl=localClient module=abci-client msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start impl=EventBus module=events msg={} server=node
May 16 13:12:14 staketab humansd[3327]: 1:12PM INF service start impl=PubSub module=pubsub msg={} server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF service start impl=IndexerService module=txindex msg={} server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF ABCI Handshake App Info hash="��\x1c�c\x13n�/m�\x19��M64U�c\x13��\x12\x1b���.,!�" height=71727 module=consensus protocol-version=0 server=node software-version=0.2.1
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF ABCI Replay Blocks appHeight=71727 module=consensus server=node stateHeight=71727 storeHeight=71727
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Completed ABCI Handshake - CometBFT and App are synced appHash="��\x1c�c\x13n�/m�\x19��M64U�c\x13��\x12\x1b���.,!�" appHeight=71727 module=consensus server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Version info abci=0.17.0 block=11 cmtbft_version=0.34.27 commit_hash= p2p=8 server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF This node is a validator addr=B8C7E45D40944E08CA38CEBE1262C4306A71E985 module=consensus pubKey=Cl+hB8Iyx/UQfY7ey2k0DP+S3/4+pb4uCy2r4wjRT9w= server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF P2P Node ID ID=b1f13e9971cfdcf784fb0efbd1b72417d5410a02 file=/root/.humansd/config/node_key.json module=p2p server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Adding persistent peers addrs=["2631445e3d6b93a5f717f14b27a5b057b88b7d9a@65.108.224.156:28656","0ab5a0c4fd3d85462da5fa149f3eb6d5702a4f32@118.193.37.229:26656","054c81f412213c90e77b295d6061a4a4b34d8f8f@141.95.99.214:14356","ca1e46048e4a9b65d60bc9e749aa431401f34ed7@144.76.45.59:26656","e6489cf86b51fa37cae968ccbbda1da03b742a5e@128.140.56.206:26656","69a6d587d4bd0d9f37404dbc03029c6220bde175@81.30.157.35:19656","b9767aa2312748caaf67425890768d85186b69b1@5.9.87.205:26646"] module=p2p server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Adding unconditional peer ids ids=[] module=p2p server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Add our address to book addr={"id":"b1f13e9971cfdcf784fb0efbd1b72417d5410a02","ip":"0.0.0.0","port":26656} book=/root/.humansd/config/addrbook.json module=p2p server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF service start impl=Node msg={} server=node
May 16 13:12:15 staketab humansd[3327]: 1:12PM INF Starting pprof server laddr=localhost:6060 server=node
```