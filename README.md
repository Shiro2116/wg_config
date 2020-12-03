### usage

Running as root.

#### Quick Installation
```bash
$ apt update && apt upgrade -y && apt install curl wget -y
$ wget -O install-wireguard.sh "https://raw.githubusercontent.com/satriaajiputra/wg_config/conf/install-wireguard.sh" && chmod +x install-wireguard.sh && ./install-wireguard.sh
```

#### start wireguard

```bash
wg-quick up wg0
```

#### access the wg_config
Access the wg_config directory first before using the script
```bash
cd ~/wg_config
```

#### add a user

```bash
./user.sh -a alice
```

This will generate a client conf and qrcode in current directory which name is alice
and add alice to the wg config.

#### delete a user

```bash
./user.sh -d alice
```
This will delete the alice directory and delete alice from the wg config.

#### view a user

```bash
./user.sh -v alice
```
This will show generated QR codes.


#### clear all

```bash
./user.sh -c
```
