# Linux Server Configuration, Udacity Project

Final project of Udacity's full stack developer program.

## Table of Contents

- Instance information
- Web Application informations
- Summary of used software
- Support

## Instance informations

The instance is hosted at:

- IP: 3.10.154.0
- SSH port: 2200

## Web Application informations

- URL: http://3.10.154.0.xip.io/

## Summary of used software

### ufw

    # ufw is used to manage firewall allowed   # this is a summary of firewall status:

    sudo ufw status
    # output
    Status: active

    To                         Action      From
    --                         ------      ----
    123                        ALLOW       Anywhere                  
    80/tcp                     ALLOW       Anywhere                  
    2200/tcp                   ALLOW       Anywhere                  
    123 (v6)                   ALLOW       Anywhere (v6)             
    80/tcp (v6)                ALLOW       Anywhere (v6)             
    2200/tcp (v6)              ALLOW       Anywhere (v6

### postgresql

- I used postgresql, active at port 5432.  
- The user `catalog` was created.  
- The database `catalogdb` was created.  
- The following previleges are granted for this user.  

```sql
GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA public TO catalog;
```

### apache2

- I used apache2 to handle requests.
- Configuration file of apache2 for this webserver is in `/etc/apache2/sites-available/catalogApp.conf`  

### ssh

- Connection over public/private key are created for the default `ubuntu` user, and for the added `grader` user.
- The location of the created `grader` user public (server side) ssh key is in: `/home/grader/.ssh/authorized_keys`


## Support

Please [open an issue](https://github.com/fraction/readme-boilerplate/issues/new) for support.
