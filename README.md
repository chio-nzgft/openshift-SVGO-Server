How to Run Go-SVGO on OpenShift
===============================

OpenShift is a great PaaS offering by Red Hat. At the moment 
Go is not currently on the supported platform list. However Red Hat 
have kindly provided a DIY cartridge to run whatever you want on the 
platform. As Go is one of my favourite languages I thought I'd put 
together a template that can be used to deploy a basic Go application. 

1. Create a new application 

    rhc-create-app --app *your-appname* --type diy-0.1 --rhlogin *your-login*

2. Add this as an upstream repository

    git remote add upstream -m master git://github.com/chio-nzgft/openshift-SVGO-Server.git
    git pull -s recursive -X theirs upstream master

3. Push to your OpenShift repository
   
    git commit -a -m "svgo openshift application"   
    git push


4. You are good to Go! You can read more about the OpenShift DIY cartridge
http://golang-nzgft.rhcloud.com/

5. you can rewrite service/mian.go and rebuid it .

