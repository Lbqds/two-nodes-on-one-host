Please download the full node from the release page: https://github.com/alephium/alephium/releases

Run the first node:

```shell
cd node0
ALEPHIUM_HOME=./ java -jar alephium-xxx.jar
```

You can see logs similar to the following from the first node:

```
2024-05-31 12:06:30,041 [main]          INFO  o.a.f.s.Configs$                       - Using user configuration file at ./user.conf

2024-05-31 12:06:30,066 [main]          INFO  o.a.f.s.Configs$                       - Using system configuration file at ./network-7/system.conf

2024-05-31 12:06:30,072 [main]          INFO  o.a.f.s.Configs$                       - Using network configuration file at ./network-7/network.conf

2024-05-31 12:06:31,034 [-dispatcher-4] INFO  a.e.s.Slf4jLogger                      - Slf4jLogger started
2024-05-31 12:06:32,185 [-dispatcher-4] INFO  o.a.f.n.CliqueManager                  - Start intra and inter clique managers, cliqueId: 031a0431bdea93cf812d0dfe2504e4be36581ed33501d5ea82164217694dc0d6d0
2024-05-31 12:06:32,190 [-dispatcher-7] INFO  o.a.f.n.CliqueManager                  - Intra clique manager is ready
2024-05-31 12:06:32,195 [dispatcher-12] INFO  o.a.f.n.TcpController                  - Node bound to /0:0:0:0:0:0:0:0:9973
2024-05-31 12:06:32,197 [-dispatcher-4] INFO  o.a.f.h.TxHandler                      - Start to load persisted pending txs
2024-05-31 12:06:32,201 [dispatcher-11] INFO  o.a.f.n.DiscoveryServer                - UDP server bound to /0.0.0.0:9973
2024-05-31 12:06:32,206 [-dispatcher-4] INFO  o.a.f.h.TxHandler                      - Load persisted pending txs completed, valid: #0, invalid: #0 (not precise though..)
2024-05-31 12:06:32,207 [main]          INFO  o.a.app.BootUp                         - Build info: name: alephium-app, scalaVersion: 2.13.10, sbtVersion: 1.6.2, commitId: 952652fa7cdc3c84054a9168022342765e8c11bd, branch: 952652fa7cdc3c84054a9168022342765e8c11bd, releaseVersion: 2.14.9
2024-05-31 12:06:32,208 [main]          INFO  o.a.app.BootUp                         - Genesis digests: 3b877620-f9d22f41-a55a2ac2-1284af43-9019ffb4-801a1465-a7ce72b6-28dc3897-05e623b8-5ce78379-f98c938a-9c277d3b-11591e8c-5dcec0fd-8004ddfe-09569e4f
2024-05-31 12:06:32,208 [main]          INFO  o.a.app.Server$Impl                    - Starting service: Server

2024-05-31 12:06:33,218 [dispatcher-11] INFO  o.a.f.n.DiscoveryServer                - Initial P2P discovery is done: #0 neighbors
2024-05-31 12:06:33,344 [main]          WARN  i.n.r.d.DnsServerAddressStreamProviders - Can not find io.netty.resolver.dns.macos.MacOSDnsServerAddressStreamProvider in the classpath, fallback to system defaults. This may result in incorrect DNS resolutions on MacOS. Check whether you have a dependency on 'io.netty:netty-resolver-dns-native-macos'
2024-05-31 12:06:33,726 [main]          INFO  o.a.w.s.WalletService$Impl             - Starting service: WalletService

2024-05-31 12:06:33,727 [main]          INFO  o.a.f.c.Node$Default                   - Starting service: Node

2024-05-31 12:06:33,728 [main]          INFO  o.a.a.WebSocketServer                  - Starting service: WebSocketServer

2024-05-31 12:06:33,728 [main]          INFO  o.a.app.RestServer                     - Starting service: RestServer

2024-05-31 12:06:33,728 [main]          INFO  o.a.h.EndpointSender                   - Starting service: EndpointSender

2024-05-31 12:06:33,760 [ol-3-worker-5] INFO  o.a.a.WebSocketServer                  - Listening ws request on 11973
2024-05-31 12:06:33,760 [ol-3-worker-3] INFO  o.a.app.RestServer                     - Listening http request on 12973
2024-05-31 12:06:33,763 [dispatcher-11] INFO  o.a.f.m.MinerApiController             - Miner API server bound to /127.0.0.1:10973
```

Run the second node:

```
cd node1
ALEPHIUM_HOME=./ java -jar alephium-xxx.jar
```

You can see logs similar to the following from the second node:

```
2024-05-31 12:06:52,376 [main]          INFO  o.a.f.s.Configs$                       - Using user configuration file at ./user.conf

2024-05-31 12:06:52,399 [main]          INFO  o.a.f.s.Configs$                       - Using system configuration file at ./network-7/system.conf

2024-05-31 12:06:52,406 [main]          INFO  o.a.f.s.Configs$                       - Using network configuration file at ./network-7/network.conf

2024-05-31 12:06:53,263 [-dispatcher-5] INFO  a.e.s.Slf4jLogger                      - Slf4jLogger started
2024-05-31 12:06:53,988 [dispatcher-11] INFO  o.a.f.n.CliqueManager                  - Start intra and inter clique managers, cliqueId: 0245fd3cb178438dbc452dada4dac4347bdb64d14cb1c14dd21c8a32fb78f3af37
2024-05-31 12:06:53,990 [dispatcher-14] INFO  o.a.f.n.CliqueManager                  - Intra clique manager is ready
2024-05-31 12:06:53,997 [dispatcher-11] INFO  o.a.f.n.TcpController                  - Node bound to /0:0:0:0:0:0:0:0:19973
2024-05-31 12:06:54,000 [dispatcher-13] INFO  o.a.f.n.DiscoveryServer                - UDP server bound to /0.0.0.0:19973
2024-05-31 12:06:54,007 [main]          INFO  o.a.app.BootUp                         - Build info: name: alephium-app, scalaVersion: 2.13.10, sbtVersion: 1.6.2, commitId: 952652fa7cdc3c84054a9168022342765e8c11bd, branch: 952652fa7cdc3c84054a9168022342765e8c11bd, releaseVersion: 2.14.9
2024-05-31 12:06:54,009 [main]          INFO  o.a.app.BootUp                         - Genesis digests: 3b877620-f9d22f41-a55a2ac2-1284af43-9019ffb4-801a1465-a7ce72b6-28dc3897-05e623b8-5ce78379-f98c938a-9c277d3b-11591e8c-5dcec0fd-8004ddfe-09569e4f
2024-05-31 12:06:54,009 [main]          INFO  o.a.app.Server$Impl                    - Starting service: Server

2024-05-31 12:06:54,059 [dispatcher-11] INFO  o.a.f.n.DiscoveryServer                - Adding a new peer: BrokerInfo(CliqueId(hex"031a0431bdea93cf812d0dfe2504e4be36581ed33501d5ea82164217694dc0d6d0"),0,1,/192.168.1.34:9973)
2024-05-31 12:06:54,093 [dispatcher-14] INFO  o.a.f.n.InterCliqueManager             - Connected to /192.168.1.34:58957
2024-05-31 12:06:55,001 [dispatcher-14] INFO  o.a.f.n.i.InboundBrokerHandler         - Self synced with /192.168.1.34:58957
2024-05-31 12:06:55,011 [dispatcher-11] INFO  o.a.f.n.DiscoveryServer                - Initial P2P discovery is done: #1 neighbors
2024-05-31 12:06:55,216 [main]          WARN  i.n.r.d.DnsServerAddressStreamProviders - Can not find io.netty.resolver.dns.macos.MacOSDnsServerAddressStreamProvider in the classpath, fallback to system defaults. This may result in incorrect DNS resolutions on MacOS. Check whether you have a dependency on 'io.netty:netty-resolver-dns-native-macos'
2024-05-31 12:06:55,537 [main]          INFO  o.a.w.s.WalletService$Impl             - Starting service: WalletService

2024-05-31 12:06:55,538 [main]          INFO  o.a.f.c.Node$Default                   - Starting service: Node

2024-05-31 12:06:55,538 [main]          INFO  o.a.a.WebSocketServer                  - Starting service: WebSocketServer

2024-05-31 12:06:55,538 [main]          INFO  o.a.app.RestServer                     - Starting service: RestServer

2024-05-31 12:06:55,538 [main]          INFO  o.a.h.EndpointSender                   - Starting service: EndpointSender

2024-05-31 12:06:55,566 [ol-3-worker-5] INFO  o.a.a.WebSocketServer                  - Listening ws request on 21973
2024-05-31 12:06:55,566 [ol-3-worker-1] INFO  o.a.app.RestServer                     - Listening http request on 22973
2024-05-31 12:06:55,569 [dispatcher-14] INFO  o.a.f.m.MinerApiController             - Miner API server bound to /127.0.0.1:20973
```
