Spam 
Installation
 
Step 1 install & activate nodebb-plugin-spam-be-gone:
 
On nodebb after logged in as admin, go to:  Admin>Plugins>Install Plugins
 
Here you search for your specific plugin, in this case nodebb-plugin-spam-be-gone.
Install the plugin, then activate it by clicking “activate”.
Once activated go to Dashboards>Overview and on your right press “rebuild & restart”.
Once it has loaded, update browser and you should now be ready to setup keys for each service you would like to use.
 
Step 2 Setting up keys & configure plugins for all services:
 
From start forum page Go to Admin>PLUGINS>Spam Be Gone
 
Service 1 Akismet: Follow the link akismet.com to get API key. There you need to register first in order to receive the key. Also here you are able to decide the minimum reputation level to classify flagged posts as false positives (HAM). Posts made by users with at least this level reputation will never be flagged as spam.
Also you can allow users with minimum reputation of X to submit posts to Akismet as spam via flagging (leave blank to disable).
 
Service 2 Project Honeypot:
Follow link projecthoneypot.org and get Honeypot API key. Register to obtain the key.
 
Service 3 Google reCAPTCHA:
Here you can sign up if you want at to obtain keys at google.com/recatcha, but if you want for the purpose of testing locally then check out reCAPTCHA documentation:
https://developers.google.com/recaptcha/docs/faq#id-like-to-run-automated-tests-with-recaptcha.-what-should-i-do
and then get these testing keys:
Site key: 6LeIxAcTAAAAAJcZVRqyHh71UMIEGNQ_MxjiZKhI
Secret key: 6LeIxAcTAAAAAGG-vFI1TnRWxMZNFuojJ4WifJWe
The reCAPTCHA widget will show a warning message to claim that it's only for testing purpose. Please do not use these keys for your production traffic.
Service 4: StopForumSpam:
Get keys from stopforumspam.com/keys. Simply add your website and generate the key to add to nodebb.
Service 5: Google hCAPTCHA
Go to https://dashboard.hcaptcha.com and get one site key and one secret key. On the website, Add the sites and hostnames on which to serve hCaptcha.
 
For some services, in order to get the keys and run the service on localhost you need to change your hosts file. For example, You can do that in /etc/hosts where you add or change for example:
127.0.0.1 test.mydomain.com
Instead of
127.0.0.1 localhost
 
Step 3 Restart:
Save each change to services. Then go back to Admin>Dashboards>Overview and click “restart” in order for it all to take effect.
