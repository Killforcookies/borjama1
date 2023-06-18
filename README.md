# borjama1
wget -q -O aleo_snarkos3.sh https://api.nodes.guru/aleo_snarkos3.sh && chmod +x aleo_snarkos3.sh && sudo /bin/bash aleo_snarkos3.sh
cat $HOME/aleo/account_new.txt
grep "prover" /etc/systemd/system/aleo-prover.service | awk '{print $5}'
journalctl -u aleo-prover -f -o cat
journalctl -u aleo-client -f -o cat
systemctl stop aleo-prover
systemctl restart aleo-client
wget -q -O aleo_remove_snarkos.sh https://api.nodes.guru/aleo_remove_snarkos2.sh && chmod +x aleo_remove_snarkos.sh && sudo /bin/bash aleo_remove_snarkos.sh
