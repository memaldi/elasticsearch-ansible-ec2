1. Set AWS credentials at ~/.aws/credentials
2. Download SSH private key at ~/.ssh/vockey.pem
3. Set the proper permissions for the key: `chmod og-rwx ~/.ssh/vockey.pem`
4. Install requirements: `pip install -r requirements.txt`
5. Install vim and less: `sudo apt update && apt install -y vim less`
6. Edit `inventory.yml` file and replace each server **public** DNS with the current ones. For the elasticsearch_host node, you must use before created hadoop_master DNS.
7. Install elasticsearch: `ansible-playbook -i inventory.yml --key-file=~/.ssh/vockey.pem --user ec2-user install-elasticsearch.yml`

