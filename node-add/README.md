
## cli1里操作：
./node-add.sh up

注意：需要把现有的 crypto-config/ordererOrganizations 移到此目录的 crypto-config

## 在被增加node 里操作
scripts 改名为 add-scripts

```bash
cd ~/official/zig-test/network/zigledger/node-add/mulhost-zig/org3-artifacts/
scp -r root@192.168.0.39:/root/zig-test/network/zigledger/node-add/mulhost-zig/org3-artifacts/crypto-config .
```

./org3-up.sh up


## 在cli1里操作：
docker exec mulhost-zig_cli_1 ./scripts/step3org3.sh


## 在被增加节点里操作
docker exec mulhost-zig_Org3cli_1 ./scripts/testorg3.sh
