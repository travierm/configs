# Setting up Laravel on a LAMP Server

## Node with NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash

nvm install stable
```

## Yarn
```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt update && sudo apt install --no-install-recommends yarn
```

## PHP Composer
```
wget https://raw.githubusercontent.com/composer/getcomposer.org/76a7060ccb93902cd7576b67264ad91c8a2700e2/web/installer -O - -q | php -- --quiet
mv composer.phar /usr/local/bin/composer
```

## PHP Deps
```
sudo apt-get install php-curl php-mbstring php-dom php-zip
```

## Certbot
```
sudo certbot --apache -d your_domain
```
