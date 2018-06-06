# hvblog
Blog using Hexo and Hexo MyAdmin Dashboard

## USAGE

```bash
    #clone
    git clone https://github.com/darshitvvora/hvblog.git
    # install 
    npm i 

    # start server with global hexo-cli
    hexo server

    # or with pm2 as deamon
    pm2 start node_modules/.bin/hexo -- server

    # visit localhost:4000 for blog
    # visit localhost:4000/admin for admin
    # username: test
    # password: Pass@123
```
  
## Bcrypt Password protection for admin

Modify config variables to your hexo `_config.yml`:

```
admin:
  username: <<your username here>>
  password_hash: <<bcrypted password here>>
  secret: <<some secret passphrase here>>
```

The `<<bcrypted password here>>` is the bcrypt hash.
Use [this
site](https://www.bcrypt-generator.com/) to generate your password. 
The `<<some secret passphrase here>>` is complicated string that is used for cookie based protection