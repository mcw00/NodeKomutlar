# NodeKomutlar
node kurulurken kullanılan komutlara örnekler
## Cüzdan ismini öğrenme:
>nodeismi keys list
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
## Delege komutu
>nodeismi tx staking delegate ValidatorAdress 'tokenAdedi''tokenİsmi' --from=Cüzdanİsmi --chain-id='test-ağı-ismi' --gas=auto
## Redelegate komutu
>nodeismi tx staking redelegate bizimValidatorAdresimiz HedefValidatorAdresi 'tokenAdedi''tokenİsmi' --from=Cüzdanİsmi --chain-id='test-ağı-ismi' --gas=auto
## Ödül Withdraw komutu
>nodeismi tx distribution withdraw-all-rewards --from=Cüzdanİsmi --chain-id='test-ağı-ismi' --gas=auto
## Undelege komutu:
>nodeismi tx staking unbond valoperaddress 'tokenAdedi''tokenİsmi'  --chain-id 'test-ağı-ismi' --from Cüzdanİsmi  --gas=auto
## jailden çıkış kodu
>seid tx slashing unjail \
  --broadcast-mode=block \
  --from=Cüzdanİsmi \
  --chain-id='test-ağı-ismi' \
  --gas=auto



