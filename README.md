# pingscan
Enter the subnet(first three octect) then this script give only live IP of that given IP.

!#/bin/bash
#Simpleping scrip
echo "Enter the subent"
read Subnet
for i in $(seq 1 255); do
      ping -c 1 $Subnet.$i | grep 'ttl=64' | cut -d " " -f 4
done
