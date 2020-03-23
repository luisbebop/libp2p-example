# libp2p-example

This is an example of a decentralized key value store using libp2p and Kademlia.

It also uses mDNS to sync nodes on the same network, if the network allows it.

The node will attach to the port `30333`.

When the node start you can use 2 commands: `PUT` and `GET`.

The key value store will be replicated between all nodes on the network.


## Setup

```
# install rust
$ curl https://sh.rustup.rs -sSf | sh -s -- -y

# run 1st node
$ cargo run

# run 2nd node
# /ip4/35.223.157.48/tcp/30333 is the address of the first node
# QmSnySq2WeXVrvF767DAkucmwCwNLAvZ5nhoEiUYUNc9f5 is the peer id of the first node
$ cargo run /ip4/35.223.157.48/tcp/30333 QmSnySq2WeXVrvF767DAkucmwCwNLAvZ5nhoEiUYUNc9f5
```

## Use

```
$ PUT foo bar
$ GET foo
```