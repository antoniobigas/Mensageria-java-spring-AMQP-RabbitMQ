# Mensageria Java SPRING AMQP e RabbitMQ


 <b>Tecnologias utilizadas:</b>
<div  align="left" dir="auto" style="display: inline_block"> <br>
<img alt="Bigas-Java" height="60" width="50"  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" />
<img alt="Bigas-Spring" height="60" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original-wordmark.svg" />
<img alt="Bigas-Docker" height="60" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg" />


</div>

# Descrição


Esse projeto está associado ao curso da DIO - Digital Innovation One - utilizando Java para criar um ambiente de 
comunicação assíncrona com o sistema RabbitMQ. Se quiser saber mais sobre o sistema de mensageria RabbitMQ
acesse: https://simplificandoredes.com/rabbitmq-1-o-que-sao-sistemas-de-mensageria/.

Neste projeto foi utilizado a versão 11 do Java e a API spring-rabbitmq. Dessa forma, foram criados ambientes distintos de comunicação
por sistema de mensageria. Os cenários dos casos de uso estão descritos na próxima seção.

Quanto ao sistema de mensageria, utilizamos o RabbitMQ instalado em um ambiente de container (virtualização) com docker.
Para instalação e configuração do Docker acesse: https://simplificandoredes.com/docker-instalacao/.

O acesso ao RabbitMQ foi realizado em curso via terminal, web API e através da interface Portainer.
Caso tenha interesse em utilizar o Portainer.io acesse: https://simplificandoredes.com/portainer-instalacao-e-configuracao/


# Conteúdo
A raiz contem uma arquivo denominado docker-compose.yml. Portanto, este arquivo não faz parte do projeto Java Spring. Mova-o para a uma pasta dedicada 
ao docker-compose. Continuando ... Este arquivo, possui as configurações utilizadas para criar o container com imagem 
RabbitMQ. Dessa formal, foram setados alguns parâmetros como: restart com sistema do host, mapeamento de dados entre host e container, imagem 
utilizada do docker hub.

Arquivo: <a href="https://github.com/antoniobigas/Mensageria-java-spring-AMQP-RabbitMQ/blob/main/Mensageria/docker-compose.yml">Docker-Compose</a>

Caso você ainda não conhece os conceitos de virtualização e as vantagens do docker, 
acesse esse artigo com a descrição toda dessa ferramenta. Link: https://simplificandoredes.com/docker-instalacao/.

Os exemplos estão organizados como segue:

demo - exemplo simplificado de troca de mensagens em sistema de filas "puro";

Work Queue - simulando processamento decorrente de mensagens com payload "pesado" (ex:simulando imagens);

Pub/Sub - comunicação utilizando a intermediação da exchange do tipo fanout;

Routing - defindo labels através da routing key;

Topic - utilizando exchange do tipo topic na comunicação;

PubConfirmation - utilizando confirmação de envio de mensagens do produtor à exchange;

DLX - Criando e utilizando uma Dead Letter Exchange para mensagens com TTL expirado.




