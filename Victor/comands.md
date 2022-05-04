code -R pasta 
code . pasta

## Para ambiente de desenvolvimento
- Desative o cache através dos módulos:(Liste os módulos: php bin/magento cache:status)
    - block_html
    - full_page

php bin/magento cache:disable 