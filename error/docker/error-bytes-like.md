# Problema
 - ERROR: for php74_db_1  a bytes-like object is required, not 'str'
 - ERROR: for db  a bytes-like object is required, not 'str'
 - File "/usr/lib/python3/dist-packages/docker/api/client.py", line 261, in _raise_for_status
 - File "/usr/lib/python3/dist-packages/requests/models.py", line 941, in raise_for_status
 - raise HTTPError(http_error_msg, response=self)
 - requests.exceptions.HTTPError: 500 Server Error: Internal Server Error for url: http+docker://localhost/v1.22/containers/69ca539d77abfa5247fc43157ea30e08a0ed2e062bcecebec68a4246cb5bbebf/start
 - docker.errors.APIError: 500 Server Error: Internal Server Error ("b'driver failed programming external connectivity on endpoint php74_db_1 (a192ca70f0c5ac5da39b0b30dcf299cf027473d1ebc38edcdfeca4291c3ba40b): Error starting userland proxy: listen tcp4 0.0.0.0:3306: bind: address already in use'")

  - Esse problema é causado devido alguma aplicação estar usando a mesma porta que o container docker, geralmente isso acontece com o mysql

# Processos
 - Abra duas abas do terminal, uma para rodar comandos de verificação e outra para comandos de ação
 - Na aba de verificação rode "sudo lsof -i -P -n", ela mostrara as aplicação e suas portas em uso, no exemplo de erro que mostrei a cima a porta em questão é a "3306" então na lista de portas eu procuro por esse valor
 - Na aba de ação tente rodar "sudo /etc/init.d/mysqld stop" ou  "sudo /etc/init.d/mysql stop"
 - Caso der tudo certo rode o comando "sudo lsof -i -P -n" novamente e vai perceber que a porta em uso não estara mais lá
 - Rode o comando "docker-compose up -d" e deve funcionar

 # Para mais informações
 - https://devops.stackexchange.com/questions/10039/internal-server-error-while-running-docker-compose-to-install-gitlab
 - https://github.com/grocy/grocy-docker/issues/26  
 - https://cafetiria.wordpress.com/2015/03/11/como-reiniciar-o-mysql-no-linux/
 - https://professor-falken.com/pt/linux/como-comprobar-si-un-puerto-esta-en-uso-en-linux-o-unix/#:~:text=Como%20verificar%20quais%20portas%20est%C3%A3o,em%20um%20sistema%20de%20processo 
