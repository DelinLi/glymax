# glymax
For www.glymax.site for sensor data visualization.

### Use Rshiny to build the website
1. [Set up of Rshiny server)[https://weihanglo.tw/debian-R-setup/doc/other_nginx.html]
<pre>
sudo apt-get install gdebi-core
wget https://download3.rstudio.org/ubuntu-14.04/x86_64/shiny-server-1.5.16.958-amd64.deb
sudo gdebi shiny-server-1.5.16.958-amd64.deb
</pre>
2. [to-do] Use NGINX to host the R Shiny server to support multiple domains on the same server. 
### Problems and Solution
1. The app.R died with error "createTcpServer: address already in use", use `lsof -wni tcp:port` find which PID is using the port, then `**kill -9 PID**`   
2. The port is failed to access   
<pre>
sudo firewall-cmd --zone=public --add-port=3838/tcp --permanent
sudo firewall-cmd --reload
</pre>


