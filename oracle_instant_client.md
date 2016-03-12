#Oracle Database Instant Client Installation

Download 
    
    cd /opt
    sudo unzip instantclient-sdk-linux.x64-12.1.0.2.0.zip
    sudo unzip instantclient-basic-linux.x64-12.1.0.2.0.zip
    
    cd /opt/instantclient_12_1
    sudo ln -s libclntsh.so.12.1 libclntsh.so
    sudo ln -s libocci.so.12.1 libocci.so
    
Install php7.0-dev
Install pecl
    
    sudo pecl install oci8-2.1.0
    instantclient,/opt/instantclient_12_1

Add extension to php.ini
Check
 
    php -i | grep oci
