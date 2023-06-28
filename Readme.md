   # ELK Stack Installation Guide

   This guide will help you install the ELK stack using Docker and Docker Compose.

   ## Prerequisites

   - Docker
   - Docker Compose

   ## Installation Steps

   1. Clone this repository - git clone https://github.com/chandan78/docker-elk-8.1.1.git
   2. Navigate to the directory containing the `docker-compose.yml` and `logstash.conf` files.
   3. Run `docker-compose up -d` to start the ELK stack.

   ## Credentials

   The default username and password for Elasticsearch and Logstash are as follows:

   - Username: YourUsername
   - Password: YourPassword

   Replace `YourUsername` and `YourPassword` with your actual username and password in docker-compose file.
   Also Replace username and password in logstash.conf file as well.

# Open elk in browser 
- http://<public ip of your server>:5601
- Note: Allow port - 9200,5601 in security of Ec2 for that server

## Enter Enrollment Key in ELK
1. Enter in elasticserach server by typing
   - sudo docker exec -it <conatiner-id> bash
   - cd ./bin/elastic-create-enrolment-token
   - copy that key and paste it in elk dashboard
2. Enter verfication code for kibna
   - sudo docker exec -it <conatiner-id> bash
   - cd ./bin/kibna-verfication-code
   - copy that code and paste it in elk dashboard