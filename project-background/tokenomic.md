# tokenomic
主要分成两大块
## BondingCurve机制
通过BC这个数学曲线来控制价格与供给的关系，请认真理解这段话的逻辑，是价格与供给关系的控制，这个机制**完全没法**用来单一的控制价格，个人觉得有两点好处
- BC机制本身有比较好的实际经济参考价值
- BC是部署在智能合约上的，这个可以用来做bzz价格的预言机，可以根据bzz的价格来动态调整swarm上的存储成本
## 激励机制

swarm主网上线后虽然没有对bee node做质押bzz的要求，但这不代表以后就没有这个机制，以后的版本中必然是会出现质押bzz的要求的，不过可能会让bee node自行做选择，如果质押的话会有更高的激励

当前的激励模型主要是

- swap
- swear
  >
- swindle
  > 针对丢失数据场景的一个惩罚机制

目前看应该是官方还没详细设计出更灵活更合理的质押机制，《book of swarm》里面有insurance这一章节，但是很多描述实现的部分是缺失的

## 参考
- https://ethersphere.github.io/swarm-home/ethersphere/orange-papers/1/sw%5E3.pdf
- https://gist.github.com/nagydani/d5c09c331224bfbffbcbe28b347ceb8e
- https://swarmresear.ch/t/postage-payment-redistribution/66