# 1 - Configurar o apache2
- Criar um novo arquivo de configuração do site
sudo cp arquivo nov-arquivo nome novo
Alterar:
- ServerName
- ServerAlias
- DocumentoRoot
- ProxyPass

Executar o comando 

sudo a2ensite nome_config

# 2 - Configuração do hosts
1 - adicionar um novo host 
Reload apache

# 3 - Download magento

# 4 - Instalar magento
- Apague a pasta vendor
- composer install (caso necessário insira a key magento)
- php bin/magento setup:upgrade
- php bin/magento setup:di:compile

### Via composer
composer create-project --repository-url=https://repo.magento.com/ magento/project-enterprise-edition



### Ativar ElasticSearch (se necessário)

evm status
evm start
evm restart
### Crie o banco de dados

### Configurar o arquivo config inicial

# 5 - Desabilitar segurança em 2 etapas
- php bin/magento module:status -> Lista os módulos ativos
- php bin/magento module:desable 


# 6 - Colocar em modo de produção
php bin/magento deploy:mode:show -> ver o modo do magento
php bin/magento deploy:mode:set production

php bin/magento deploy:mode:set developer
