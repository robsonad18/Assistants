# Problema
Esse erro acontece devido a um conflito de portas entre o docker e o servidor apache, as vezes eles acabam pegando a mesma porta, então para você rodar o container docker sem ocorrer problemas no acesso a porta pare os serviços apache

# Comando
sudo /etc/init.d/apache2 stop
