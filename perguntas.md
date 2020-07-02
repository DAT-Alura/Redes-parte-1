# Aula 1

O que caracteriza uma rede?
- Máquinas que estão interligadas, passando informaões em diversos pontos.
- De acordo com o site do Wikipedia, a melhor definição de redes de computadores seria: “Uma rede de computadores é formada por um conjunto de máquinas eletrônicas com processadores capazes de trocar informações e partilhar recursos”. Ou seja, pelo fato das máquinas estarem interligadas e serem capazes de trocar informações, caracterizaria uma rede.

Qual protocolo está dentro do ping?
- ICMP
- Dentro da ferramenta administrativa do ping temos o protocolo ICMP, sendo ele o responsável por mandar uma requisição (Echo Request) para máquina remota e esperar um retorno dessa máquina remota (Echo Reply).

Caso o tempo indicado no teste do ping esteja mais elevado em relação ao valor que normalmente apresenta, o que isso quer dizer?

- Isso significa que podemos ter um problema tanto na comunicação de ida ou da volta
- Quando temos um alto valor no índice do tempo do teste do ping, isso significa que podemos ter um problema em nossa comunicação. O protocolo ICMP que está dentro do ping manda um Echo request e aguarda um retorno de resposta da máquina destino (Echo Reply). Dessa forma, o tempo elevado pode indicar um problema na comunicação que pode estar tanto em um trecho como em outro.

O que seria o TTL que aparece no teste do ping?

- TTL indica por quantas máquinas (hops) minha informação pode passar antes de ser extinta
- O TTL seria uma informação dentro do pacote do IP que informa qual é a máxima quantidade de hops que minha informação pode passar antes de ser descartada. É a quantidade de máquinas que ela vai poder passar no caminho.

Quando digitamos ping www.google.com no console aparece um número, o que seria esse número?

- Endereço de IP
- Ao digitarmos www.google.com, ocorre uma tradução entre o nome e o endereço IP da máquina do google que estamos acessando. As máquinas para serem identificadas na rede devem possuir um endereçamento IP.

Qual ferramenta administrativa eu uso para testar conectividade?

- ping
- Dentro do __ping__ temos o protocolo ICMP responsável por fazer a requisição até uma máquina remota (Echo Request) e esperar a resposta (Echo Reply). Através desse protocolo ICMP, podemos verificar se temos uma resposta da máquina remota, sabendo assim se temos conectividade. O __traceroute(unix) ou tracert(win)__ seria usado para verificar a rota que minha informação percorreu até chegar o destino. O __ipconfig__ seria usado para ver as configurações de IP de minha máquina e o __nslookup__ seria para verificarmos recursos mais avançados de problemas que podemos ter entre a url e o endereço IP.

Qual o principal uso do traceroute ou tracert?

- Verificar a rota que a minha informação está passando na rede
- A principal funcionalidade do traceroute é verificar a rota que a minha informação levou para chegar até a máquina de destino. Isso porque, em redes de computadores temos o que chamamos de __rede não determinística__, ou seja, não necessariamente um pacote de informação vai ser transferido pela mesma rota do anterior com o mesmo intervalo de tempo. Isto se deve a muitos fatores, por exemplo, uma máquina que pode estar congestionada ou um problema no link de comunicação, etc. Pense como se a rede fosse uma cidade com várias ruas, nem sempre pegaremos a mesma rota para chegar até a nossa casa ou ir para o trabalho, depende de muitos fatores, por exemplo, trânsito, obras e outros aspectos. Nas redes de computadores não é tão diferente. :)

Quando eu digito tracert e vemos que uma máquina retornou a informação (*), o que isso quer dizer?

- Provavelmente o administrador da máquina desabilitou a resposta ao nosso chamado, para evitar um grande volume de tráfego na máquina bem como por questões de segurança.
- Quando nós temos uma máquina que retornou (*) e passou a informação para uma próxima máquina, isso provavelmente indica que o administrador dessa máquina desabilitou a resposta ao nosso chamado. O que acontece seria que esse tipo de teste pode ser interpretado como uma tentativa de “scanear” possíveis portas abertas e vulnerabilidades que possam existir, caso seja usado por um usuário malicioso, pode ser usada como uma forma de reconhecimento da rede dessa possível vítima para que assim possa explorar possíveis falhas.

# Aula 2

Qual a responsabilidade do servidor DNS?

- Traduz URLs para endereços IP
- Os servidores __DNS__ são chamados de __Domain Name Servers__ e sua função é realizar o __“mapeamento”__ entre endereço IP e url (ex: www.google.com). Dessa forma, se estamos digitando www.google.com no browser, o servidor DNS está fazendo a tradução entre o nome da url e o endereço IP.

Qual o nome que damos quando configuramos um endereço IP manualmente em nosso computador?

- IP estático
- __Quando inserimos um IP em uma máquina__, ela passa a atuar com aquele endereço IP, esse tipo de inserção manual de endereço IP é chamado de __IP estático__, pois fixamos que ele tenha o valor que inserimos.

Qual principal uso do nslookup?

- Verificar traduções de nomes de domínios e endereços IP e isolar problemas entre as duas partes
- O Nslookup pode ser usado para descobrirmos o endereço IP de um domínio, bem como saber detalhes mais avançados de DNS, para saber se nosso serviço está sendo direcionado para a máquina de destino, por exemplo.

Ao digitar nslookup www.google.com eu recebo uma mensagem de resposta não autoritativa, por que recebo essa mensagem?

- Porque quem respondeu foi uma __máquina da minha rede local__ que __guardou a informação do site que havia acessado previamente__ e ela que está respondendo pela requisição.
- Uma vez que eu já acessei o site antes, essa máquina guarda em sua memória, para não ter que ficar fazendo essas requisições na internet o tempo todo. Dessa forma, a minha máquina que respondeu não tem autoridade sobre esse domínio, não é minha máquina que possui o registro do www.google.com.

Como funciona o ping?

- Ele manda uma requisição para a máquina que procuramos (Echo Request) e aguarda uma informação de retorno (Echo Reply)
- O ping possui dentro dele um protocolo chamado __ICMP__, ele vai mandar uma requisição (Echo request) e aguarda uma resposta (Echo reply).

Qual equipamento podemos usar para conectar vários computadores?

- Hub
- O __Hub__ é um equipamento utilizado para interconectar diversos dispositivos finais. __NAT__ é um método de tradução de endereços privados e públicos. __Servidor__ é uma máquina centralizada que oferece serviços a um cliente (ex: computador). __Máscara de rede__ é usado para determinar se dois equipamentos estão na mesma rede.

# Aula 3

Quais são os dois tipos de cabos que usamos para conexão?

- Cabo direto e cabo cruzado
- Caso tenhamos o mesmo padrão de cores na duas pontas do cabo, chamamos de cabo direto, pois as mesmas cores estão nas mesmas posições nas duas pontas. Caso tenhamos um padrão de cores diferente em cada ponta do cabo, teremos o que chamamos de cabo cruzado.

O que caracteriza um cabo cruzado?

- Um cabo que possui os fios internos em posições diferentes em cada ponta
- Quando temos um padrão de cores diferente em cada ponta do cabo, teremos o que chamamos de cabo cruzado.

O que caracteriza um cabo direto?

- Um cabo com a mesma sequência de cor nas mesmas posições nas duas pontas do cabo
- Quando temos um padrão de cores iguais nas duas pontas do cabo, teremos o que chamamos de cabo direto

Quais são os dois padrões feitos pela TIA?

- T568A e T568B
- O padrão de cores feitos pela TIA seria T568A e T568B, sendo que a T568A possui a sequência de cores, nesta ordem: branco e verde, verde, branco e laranja, azul, branco e azul, laranja, branco e marrom, marrom e a T568B: branco e laranja, laranja, branco e verde, azul, branco e azul, verde, branco e marrom, marrom

Qual tipo de cabo usamos para fazer a conexão entre dois computadores?

- Tipo cruzado
- Pelo fato de termos dois computadores, eles tem o mesmo tipo de placa de rede e vão transmitir os sinais nas mesmas posições. Dessa forma é necessário realizar essa compatibilidade entre os sinais de transmissão e recepção e isso é obtido através do cabo cruzado.

Onde é transmitido os sinais nas placas de rede dos computadores por padrão?

- Fios 1 e 2
- As placas de rede dos computadores transmitem, por padrão, nas posições 1 e 2.

Onde é recebido os sinais nas placas de rede dos computadores por padrão?

- Fios 3 e 6
- As placas de rede dos computadores recebem por padrão nas posições 3 e 6.

Onde é transmitido os sinais nas placas de rede dos hubs por padrão?

- Fios 3 e 6
- As placas de rede dos hubs transmitem por padrão nas posições 3 e 6

Onde é recebido os sinais nas placas de rede dos hubs por padrão?

- Fios 1 e 2
- As placas de rede dos hubs recebem por padrão nas posições 1 e 2.

Em um projeto precisei interconectar dois computadores diretamente, pelo fato de não ter cabo cruzado, resolvi fazer o teste com cabo direto e consegui “pingar” o outro computador. Qual é a provável razão para isso ter acontecido?

- Provavelmente as placas de rede possuem um padrão auto-MDIX que é capaz de detectar que colocamos um cabo “errado”, mas consegue realizar a correção das polaridades via software
- Algumas placas de rede mais modernas possuem o padrão auto-MDIX, dessa forma, se as duas placas de rede estiverem configuradas, elas poderão corrigir essa questão da polaridade e se comunicarem.

# Aula 4

Qual seria duas das principais limitações do Hub?

- Segurança e lentidão
- Os hubs não conseguem aprender onde está localizado cada máquina, dessa forma, ele __repassa a informação para todas as demais máquinas conectadas__. Isso quer dizer que caso ocorra um fluxo intenso de tráfego na rede, teremos essa informação sendo encaminhada para todos os demais usuários causando __lentidão na rede__. Além disso, __quando usuários mandam a informação__ destinada para um usuário específico, __os demais usuários recebem essa informação__, causando assim uma __vulnerabilidade de segurança__.

Qual a principal utilização do programa Wireshark?

- Analisar protocolos para resolver problemas em redes
- O Wireshark tem como principal utilização analisar protocolos que trafegam na rede com o intuito de verificar problemas que possam existir.

Qual desses é um protocolo utilizado para criptografar minha informação?

- TLS
- TLS (Transport Layer Security) seria um protocolo de criptografia utilizado para a segurança da informação. Ele seria a evolução do protocolo SSL (Secure Sockets Layer)

Qual seria a responsabilidade do protocolo TCP?

- Transportar minha informação
- O protocolo TCP encontra-se acima da camada onde o IP está localizado e ele é responsável por realizar o transporte da minha informação. Além do protocolo TCP, essa camada possui também outro protocolo bastante conhecido, o UDP.

Porque não foi possível visualizar a informação que o usuário (vítima) digitou na página do youtube?

- A informação estava criptografada
- O youtube usa em seu site um sistema de criptografia das informações, onde o protocolo TLS é responsável por essa atividade. Pelo fato das informações, estarem criptografadas não foi possível reconstruir a informação e visualizar o que o usuário estava digitando.