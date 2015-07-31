# Install Self Signed SSL on MacOS Yosemite 10.10.4

The following settings work on MacOS Yosemite 10.10.4 with MAMP 3.2.1. 

In addition, the guide will show you how to make Chrome *44.0.2403.125* Trust the new certificate.

#### Create the SSL certificate

1. Go to the user's root

    ```cd ~```

2. Generate a Private Key

    ```openssl genrsa -des3 -out server.key 2048```
    
    *make up a passphrase and remember it, you’ll need it 3 more times.*

3. Generate certificate signing request

	```openssl req -new -key server.key -out server.csr```
	
	*same passphrase*
	
4. Answer the following questions

	```
	Country Name: # leave blank
	State Name: # leave blank
	Locality: # leave blank
	Organization: # Name your Certificate
	Organization Unit Name: # leave blank
	Common Name: localhost
	Email address: email@example.com
	A challenge password: # leave blank
	An optional company name: # leave blank
	```
	
5. Generate the certificate from the CSR for 5 years

	```openssl x509 -req -days 1825 -in server.csr -signkey server.key -out server.crt```
	
6. Remove the password requirement from the server key

	```cp server.key server.tmp```
	
	```openssl rsa -in server.tmp -out server.key```
	
	*same passphrase*
	
#### Set up MAMP 3.2.1

1. Move the certificate files (server.key and server.crt) to:
	
	```/Applications/MAMP/conf/apache/```
	
2. Open Apache's httpd.conf file:

	```/Applications/MAMP/conf/apache/httpd.conf```
	
	```
	set your listen port to 80 (near the top of the file)
	Listen 80

	set your ServerName to localhost:80 (default is 8888)
	ServerName localhost:80
 
	uncomment the line that includes the secure (SSL/TLS) connection con
	Include /Applications/MAMP/conf/apache/extra/httpd-ssl.conf
	```
	
	Save it and close. Now open Apache's ssl conf file:
			
	```/Applications/MAMP/conf/apache/extra/httpd-ssl.conf```
	
	Find the <VirtualHost> entry (big block at the end of the file starting with <VirtualHost _default_:443> and ending with </VirtualHost>) and replace the entire thing with:
	
	```
	<VirtualHost *:443>
        SSLEngine on
        SSLCertificateFile /Applications/MAMP/conf/apache/server.crt
        SSLCertificateKeyFile /Applications/MAMP/conf/apache/server.key
	</VirtualHost>
	```
	
	Save and close. Start your MAMP server. You should be able to access your document root at 	```http://localhost``` and ```https://localhost```
	
3. Delete leftover files

	```rm ~/server.csr ~/server.tmp```
	
	
Now, when you open your Chrome you will be informed that you can proceed with viewing the https page. However, there is no easy way to make your Chrome respect your option to trust this certificate so we have to do some work to accomplish that.

####Force Chrome to trust your certificate

1. Open your Chrome browser and go to ```https://localhost```. The URL bar you will notice that the lock is red. Double-click on it and a dialogue popup, select the 'Connection' tab (second tab) and click on the link 'Certificate Information'. A new popup appears

2. Drag the image of the certificate (looks like an actual certificate with a yellow stamp) in your Desktop. The certificate is now on your desktop. 

3. Double click on the certificate and the Keychain Access Mac App pops up. Enter your password to unlock it.

4. IMPORTANT! Be sure you add the certificate to the System keychain, not the login keychain! Click "Always Trust," even though this doesn't seem to do anything.

5. After it has been added, double-click it. You may have to authenticate again.

6. Expand the "Trust" section.

7. "When using this certificate," set to "Always Trust"

That's it! Close Keychain Access and restart Chrome, and your self-signed certificate should be recognized now by the browser.

