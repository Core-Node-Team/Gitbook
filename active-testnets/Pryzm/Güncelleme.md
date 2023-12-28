# Güncellemeler

### Güncelleme Version 0.10.0 (316000)

### Güncelleme scriptini çalıştırmak için bir screen açın

```
screen -S update
```

### İndirin ve çalıştırın

```
curl -sSL -o update-0.10.0.sh https://raw.githubusercontent.com/Core-Node-Team/scripts/main/pryzm/update-0.10.0.sh && chmod +x update-0.10.0.sh && bash ./update-0.10.0.sh
```

#### Belirlenen blok yüksekliğine ulaştıktan sonra node güncellenecek

#### Screenden çıkabilirsiniz `CTRL A D` ile

#### Tamamladıktan sonra scripti silebilirsiniz `rm update-0.10.0.sh`
### Manuel güncellemek için 316000.bloğa geldiğinde
```
systemctl stop pryzmd
wget https://storage.googleapis.com/pryzm-zone/core/0.10.0/pryzmd-0.10.0-linux-amd64
chmod +x pryzmd-0.10.0-linux-amd64
mv pryzmd-0.10.0-linux-amd64 $(which pryzmd)
systemctl restart pryzmd
```
