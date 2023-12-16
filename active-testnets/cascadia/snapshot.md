# Snapshot

```bash
sudo apt install liblz4-tool

systemctl stop cascadiad

cp $HOME/.cascadiad/data/priv_validator_state.json $HOME/.cascadiad/priv_validator_state.json.backup

cascadiad tendermint unsafe-reset-all --home $HOME/.cascadiad --keep-addr-book

curl -L http://snapshot.corenode.info/cascadia_testnet/cascadia_snap.tar.lz4 | tar -I lz4 -xf - -C /.cascadiad/data

mv $HOME/.cascadiad/priv_validator_state.json.backup $HOME/.cascadiad/data/priv_validator_state.json

sudo systemctl start cascadiad && sudo journalctl -u cascadiad -fo cat
```
