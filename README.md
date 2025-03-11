# My first project
AWS monitoring code using shell scripting

we are first going to connect to the aws from our console using
"aws configure"

Post providing the "access key" and "password". we will execute the scrips used for listing all the detils like s3,ec2,Lambda,IAM users

we can add this script to cron to get details daily.

# Sort script

To sort the proper phone number from teh file.txt in single line command

we have used grep command, along with -e to include multiple regex

"[0-9]\{3\}" represents 3 numbers (\{3\}) between the range 0-9

^ is start of string. $ indicates end of the string.

\ to supress the specialness of the character.

# To Print the 10 lines

To print the 10th lines, we can use awk command. 

we need to provide the file.txt as input, and it will print 10th line

# Network monitor

To monitor and check the network connection, we can observe the connections like internet connection, DNS resolution, latency ,and internet speed

For internet connection we are using commands like ping
~~~
ping -c 4 <TARGET_IP>
~~~

For DNS resolution we are using nslookup
~~~
nslookup <TARGET_DOMAIN>
~~~

For Latency we can using ping as well
~~~
ping -c 4 <LATENCY_TARGET> | tail -n 1 | awk -F '/' '{print $5}'
~~~

For internet speed we are using program like speedtest
~~~
speedtest-cli --simple
~~~

The output is forwarded to the network_troubleshoot.log file

## dashed file (-)

A file name is of - then we cant view or open the file, we need to use fqdn for opening files like that
~~~
cat ./-
~~~
