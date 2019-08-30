# jenkinsrpm
RPM built Jenkins with basic plugins installed
Based off of this super handy repo 
https://github.com/samrocketman/jenkins-bootstrap-shared

In order to adhere to the 100M file size limit, I had to split the rpm 

split -b 50m jenkins-bootstrap-2.121.3.2-0.noarch.rpm jenkins-bootstrap-2.121.3.2-0.noarch.rpm-1

which then output three files 
youo can then concatenate them back together, as

cat jenkins-bootstrap-2.121.3.2-0.noarch.rpm-1aa jenkins-bootstrap-2.121.3.2-0.noarch.rpm-1ab jenkins-bootstrap-2.121.3.2-0.noarch.rpm-1ac >  
jenkins-bootstrap-2.121.3.2-0.noarch.rpm
