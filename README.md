  ```
	git clone https://github.com/tanst/mod.git tmp && mv tmp/.git . && rm -rf tmp && git reset --hard
	cp config/.config.php.example config/.config.php
	chattr -i .user.ini
	mv .user.ini public
	chown -R root:root *
	chmod -R 777 *
	chown -R www:www storage
	chattr +i public/.user.ini
  ```
```
/public




location / {
    try_files $uri $uri/ /index.php$is_args$args;
}
```
