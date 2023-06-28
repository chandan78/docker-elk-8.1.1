

# steps to ssh into logstash users :
Locate [ logstash_private ] key
chmod 400 logstash_private 
ssh -i "key" ubuntu@xxxxx.amazonaws.com


# For ubuntu Users :
1. Locate your private key file. The key used to launch this instance is logstash-cloudtrail-key.pem
2. Run this command, if necessary, to ensure your key is not publicly viewable.
3. chmod 400 logstash-cloudtrail-key.pem
4. ssh -i "key.pem" ubuntu@xxxx.amazonaws.com



# create new users :-
sudo adduser user_name
Enter password and other details
add to users to group
switch users : su - users_name
Generate Key - > by putty gen save public and private(pem) file 
add .ssh folder into newly created users
vim authorized_keys -> Import public key into authorized keys
use the key to ssh into machine to that users . 

# Web Hook Credentials : 

https://hooks.slack.com/services/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
curl -X POST -H 'Content-type: application/json' --data '{​​​​​​"text":"Hello, World!"}​​​​​​' https://hooks.slack.com/services/****************

# test smtp :


 ruby {
    code => "event.set('indexDay', event.get('[@timestamp]').time.localtime('+09:00').strftime('%Y%m%d'))"
  }


