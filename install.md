# Passo A Passo:

- copiar ficheiro "dev.magento.conf" e alterar ficheiro "dev.nome.conf" em /etc/apache2/sites-available
- /etc + sudo vim hosts e adicionar ip e nome do ficheiro
- criar pasta = mkdir "nome" em /var/www/html
- mover ficheiro magento ( download ) para esta pasta
- unzip pasta
- composer install
- evm start
- criar base de dados
- copiar e colar setup install magento
- sudo systemctl restart apache2
- sudo a2ensite
- systemctl reload apache2
- voltar á pasta do projeto
- php bin/magento module:status | grep Two
- php bin/magento module:disable "nome da pasta que aparece em disable"
- php bin/magento setup upgrade
- rm -rf vendor ( apagar esta pasta predefinida )
- composer install
- php bin/magento setup:upgrade
- php bin/magento deploy:mode:set production


=======================================

## Criar um USER ADMIN ->  /var/www/html/latest/ php bin/magento admin:user:create


   ============================================================
   =====	rui Magento Admin URI = admin_1hwjed        =======
   ============================================================
   
   ============================================================
   =====	exemplo Magento Admin URI = admin_ox9i2j       =======
   ============================================================




bin/magento setup:install \
--base-url=http://dev.exemplo \
--db-host=localhost \
--db-name=db_exemplo \
--db-user=root \
--db-password=toogas123 \
--admin-firstname=rui \
--admin-lastname=martins \
--admin-email=rui.martins@toogas.com \
--admin-user=rui \
--admin-password=rui1234 \
--language=en_US \
--currency=EUR \
--timezone=Europe/Lisbon \
--use-rewrites=1 \
--search-engine=elasticsearch7 \
--elasticsearch-host=localhost \
--elasticsearch-port=9200 \
--elasticsearch-index-prefix=exemplo \
--elasticsearch-timeout=15

------------------------------------------------------------------------------------------------------------------------------------------------------------------
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

