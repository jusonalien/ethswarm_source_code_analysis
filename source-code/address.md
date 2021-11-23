## Address

用来管理overlay和underlay地址的功能，其中主要包括了overlay地址和underlay地址, 
其中，
overlay地址用来标识每个bee nodes在拓扑网络结构中的位置，
underlay地址用来标识实际的物理地址，亦即IP地址，用来实现端对端的网络通讯

swarm基于kadelima协议来实现全网的所有bee nodes之间的位查找，通讯等功能，本身要维护一个DHT(Distributed Hash Table)


定义address的数据结构, bzz/address.go 文件


```go
// Address represents the bzz address in swarm.
// It consists of a peers underlay (physical) address, overlay (topology) address and signature.
// Signature is used to verify the `Overlay/Underlay` pair, as it is based on `underlay|networkID`, signed with the public key of Overlay address
type Address struct {
	Underlay        ma.Multiaddr
	Overlay         swarm.Address
	Signature       []byte
	Transaction     []byte
	EthereumAddress []byte
}
```