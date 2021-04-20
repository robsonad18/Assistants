# Problema
Quando você tenta rodar composer install ele retorna um mensagens com um erro dizendo que devidas extensões não estão abilitadas

# Processos
 - Apague a pasta vendor(caso ela tenha cido criada)
 - Apague o arquivo composer.lock(caso ele tenha cido criado)
 - Rode o comando composer install --ignore-platform-reqs ou composer update --ignore-platform-reqs
