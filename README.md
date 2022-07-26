# NodeKomutlar
node kurulurken kullanılan komutlara örnekler
## Cüzdan ismini öğrenme:
```
nodeismi keys list
```
## Yeni cüzdan oluşturma komutu:
```
nodeismi keys add
```
## Mevcut cüzdanı ekleme:
```
nodeismi keys add --recover
```
## Node durdurma komutu:
>systemctl stop nodeismi
## Node başlatma komutu:
>systemctl start nodeismi
## Node restart komutu:
>systemctl restart nodeismi
## Version Öğrenme:
>nodeismi version
## Logları izleme komutları:
>journalctl -u nodeismi -fo cat
## Node durumuna bakma komutları:
>nodeismi status 2>&1 | jq .SyncInfo
## Peer bilgisi öğrenme:
>echo "$(quicksilverd tendermint show-node-id)@$(curl ifconfig.me):26656"
## Delege komutu:
>nodeismi tx staking delegate ValidatorAdress 'tokenAdedi''tokenIsmi' --from=CüzdanIsmi --chain-id='test-ağı-ismi' --gas=auto
## Redelegate komutu:
>nodeismi tx staking redelegate bizimValidatorAdresimiz HedefValidatorAdresi 'tokenAdedi''tokenIsmi' --from=CüzdanIsmi --chain-id='test-ağı-ismi' --gas=auto
## Ödül Withdraw komutu
>nodeismi tx distribution withdraw-all-rewards --from=CüzdanIsmi --chain-id='test-ağı-ismi' --gas=auto
## Undelege komutu:
>nodeismi tx staking unbond valoperaddress 'tokenAdedi''tokenIsmi'  --chain-id 'test-ağı-ismi' --from CüzdanIsmi  --gas=auto
## Jailden çıkış komutu:
>seid tx slashing unjail \
  --broadcast-mode=block \
  --from=Cüzdanİsmi \
  --chain-id='test-ağı-ismi' \
  --gas=auto
## Config dosyasına erişim komutu:
>nano /root/.nodeismi/config/config.toml
## Oy verme komutu:
nodeismi tx gov vote 'oylamaId' yes --from CüzdanIsmi --chain-id='test-ağı-ismi' -y




