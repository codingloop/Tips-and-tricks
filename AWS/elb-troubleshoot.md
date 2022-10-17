## Steps error log file:
 `cat /var/log/cfn-init-cmd.log`

## Main log file:
`/var/log/eb-engine.log`

## Django app location in elastic beanstalk:
`/var/app/current`
 
### Adding file in ELB extendion file:
'''
files:
    "/etc/nginx/conf.d/elasticbeanstalk/0099_static.conf":
        mode: "000644"
        owner: root
        group: root
        content: |
            multiline
            location /static {
                alias /var/app/current/static;
                access_log off;
            }
'''            
