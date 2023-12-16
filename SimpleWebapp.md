# awswebap
A simple web app Hosted on AWS
1. - Login to the EC2 AWS Console.
     > https://console.aws.amazon.com/console/home
     
2. - Choose the Amazon Variant of an Instance.
3. - Switch to root user and Update Packages .
     ```linux
     sudo su - && yum update -y
     
4.  - Install Web server abd Packages .
     ``` linux 
     yum still -y httpd
5. - Check Webserver status.
      ``` linux 
      systemctl status httpd
6. - Enable Webserver .
      ``` linux 
       enable httpd
7. - Create Temp directory .
     ``` linux
     Mkdir temp
8. - Get into the directory.
      ``` linux
      cd temp/
9. - Get a template of any website of your choice.
   > [here is an example of where to get some] {https://www.free-css.com/free-css-templates}.
    
10 - Download the zip file of template of choice.
      ``` linux
      wget (template website link)
      
11 -  Unzip Downloaded website template.
        > Unzip (zipfile)
        
12 - Run ls -lrt to see all files in the zipped file.

13 - Move all Dowloaded files to Var/ directory.
       ``` linux
        Mv * /var/www/html/
        
14. - Change directory.
        ``` linux
        cd /var/www/html/
        
15. Enable and Start Webserver.
      ``` linux
      systemctl enable httpd &&  systemctl start httpd
      
16. - Check status by running webserver.
         ``` linux
         systemctl status httpd
         
17 - load new webpage.
      ``` linux
      http://<public-ip>:80
      
18. Congratulations your new Webapp running on EC2 is now live. 
