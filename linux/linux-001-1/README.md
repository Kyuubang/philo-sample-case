## sample lab with philo

### Basic web server with nginx

#### Step 1 -- Install nginx 

run nginx with following command 

```bash
sudo apt install nginx -y
```

#### Step 2 -- download lab assets

```bash
philo lab download
```

#### Step 3 -- Configure nginx 

create config file named `philo.conf` at `/etc/nginx/sites-available/`

```bash
sudo vim /etc/nginx/sites-available/philo.conf
```

copy following configuration on `philo.conf`

```nginx
server {
	listen 80 default_server;
    server_name _;
    root /var/www/html/philo;
    
    location / {
        try_files $uri $uri/ =404;
    }
}
```

enable `philo.conf` to `/etc/nginx/sites-enabled/`

```bash
sudo ln -s /etc/nginx/sites-available/philo.conf /etc/nginx/sites-enabled/
```

disable default config 

```bash
sudo unlink /etc/nginx/sites-enabled/default
```

make sure all configuration no errors found

```bash
sudo nginx -t
```

if errors found you should fix before you restart nginx, if no errors restart with following command.

```bash
sudo systemctl restart nginx
```

#### Step 4 -- Verify your work

make sure output same as example

```bash
curl localhost
```

```html
<h4>Hello, I'm philo will be assist you forever</h4>
```

or browse url on your favorite browser
