Projeto trabalhado em forma colaborativa deve ter a mesma chave no arquivo env.php

## Lista os comandos do magento

php bin/magento

## Módulos magento
Magento_TwoFactorAuth -> Autenticação em duas etapas

## Comandos úteis magento
compose install -> instala o magento

### Sincroniza o backoffice  
php bin/magento setup:upgrade
php bin/magento setup:di:compile -> Verifica se está tudo em ordem de acordo com as normas da Magento

php bin/magento deploy:mode:show -> ver o modo do magento
php bin/magento deploy:mode:set developer
php bin/magento deploy:mode:set production

php bin/magento setup:static-content:deploy -f

php bin/magento module:status -> lista os módulos
php bin/magento module:disable (modulo)
php bin/magento admin:user:create

## Comandos ElasticSearch

evm status
evm start
evm restart


## Extra
php bin/magento cache:flush -> atualização cache
