# ForgetPasworkMysqlWorkbenchMacbook

For mysql 8 in MacOS
Terminal
  stop all mysql server service
  cd /usr/local/mysql/bin
  sudo ./mysqld_safe --skip-grant-tables
  this will start mysql server in this terminal

Start new terminal
  cd /usr/local/mysql/bin
  sudo ./mysql -u root
  FLUSH PRIVILEGES;
  UPDATE mysql.user SET authentication_string=null WHERE User='root';
  FLUSH PRIVILEGES;
  exit;
  sudo ./mysql -u root
  ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'yourpasswd';
  FLUSH PRIVILEGES;
  exit;
  sudo ./mysqladmin -u root shutdown -p (this will shutdown mysql server that started at the other terminal)
  start mysql with the normal way
