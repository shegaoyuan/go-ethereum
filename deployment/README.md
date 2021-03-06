# 部署过程

## 编译
- make geth
  
## 创建钱包
- geth account new
  
## 修改genesis.json
- 用创建的地址修改extraData 初始validator配置。可将54c0092f1faE8217DAb63fec4374B1a21c1b3b7E替换为自己的地址，如果希望是多个地址，则将多个地址拼接起来替换即可。
- alloc字段修改预发行资产的地址和数量

## 初始化
- geth init genesis.json

## 运行
` geth --mine --miner.threads=1 --miner.etherbase=0x54c0092f1faE8217DAb63fec4374B1a21c1b3b7E --unlock "0x54c0092f1faE8217DAb63fec4374B1a21c1b3b7E" -rpcapi "db,eth,net,web3" `
` 运行前上述两个地址改为自己的创建的钱包地址 `
