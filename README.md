# CockroachDB-Monitoring-with-Vector
Collect CRDB metrics and logs with Vector


### Installing Vector in a CRDB node

```bash
curl -1sLf 'https://repositories.timber.io/public/vector/cfg/setup/bash.deb.sh' | sudo -E bash
sudo apt-get install -y vector
# sudo apt-get upgrade vector
# sudo apt remove vector
```

### Configure Vector

```bash
# Configure vector toml file and test it before sending it to the final location
vi vector.toml
sudo vector --config vector.toml

# Move or copy paste the tested config to:
sudo vi /etc/vector/vector.toml
```

**Note:** When configuring vector, make sure to turn off the console terminal output before executing the Daemon service

### Run Vector as a Daemon service

```
### For background process run it via systemctl [start,stop,reload,restart]
sudo systemctl start vector
sudo systemctl status vector
```
