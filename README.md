# Suricata
Suricata Setup on Ubuntu

sudo apt-get install -y suricata
where is suricata
cd /etc/suricata
# backup suricata.yaml
sudo cp suricata.yaml suricata.yaml.backup
ls
sudo nano suricata.yaml
# open another terminal - ip addr (to view inet and enpOs
# insert the inet address on $HOME_NET
# control w to search for af-packet
# insert enpOs to replace etho
# control w to search for rule-files- disable suricata.rules by adding # at the beginning 
# create custom.rules in the next line
# scroll up to interface: etho and replace with enpOs
# control O to write out and enter to save, then control x to exist
# check if yoy have suricata as directory or create
sudo mkdir suricata /var/lib
cd /var/lib/suricata/rules
sudo touch custom.rules
ls
# test suricata is working, open terminal and put command
sudo suricata -c /etc/suricata/suricata.yaml -i enpOS

# CREATE IDS RULES 


