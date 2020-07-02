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

# Aula 5

O que é o protocolo ARP?

- Quando eu não conheço um dispositivo eu lanço esse protocolo para procurar o IP que eu quero me comunicar. A máquina buscada por sua vez vai retornar informando seu endereço MAC.
- __O ARP é o protocolo utilizado para fazer o mapeamento entre o endereço IP e o endereço MAC de um dispositivo__. Isso é necessário porque o MAC encontra-se um nível abaixo do IP e eu preciso dele para poder transmitir as informações. Em redes de computadores, temos protocolos que possuem hierarquias diferentes. Para poder chegar até o IP que está na camada 3, eu preciso passar pelo MAC que está na camada 2, pense como se fosse escalar uma pirâmide, não dá pra chegar ao topo sem passar pelo meio dela!

Qual equipamento veio para substituir os hubs?

- Switches

Qual é a principal diferença entre os Hubs e os Switches?

- O Hub não consegue aprender onde um equipamento está localizado, o Switch sim.
- Os hubs não conseguem __aprender o endereço MAC__ das máquinas, já os Switches possuem essa função.

Como o Switch aprende onde um equipamento está localizado?

- Quando um dispositivo quer se comunicar com outro, ele vai necessitar passar pelo Switch e ele informa dentro do pacote qual é __seu endereço MAC__ e o __Switch grava essa informação em sua memória__.
- Os dispositivos ao se comunicarem passam pelo Switch e ao passar pelo Switch ele grava em sua memória quem está conectado em qual porta.

Qual é uma forma de ataque usada para conseguir informações passadas no Switch destinadas a outro usuário?

- Colocar vários endereços MAC falsos para __“lotar” a memória do Switch__ e fazer com que ele __atue como um Hub__.
- Métodos usados por usuários maliciosos seria de inserir vários endereços MAC falsos para “lotar” a memória do Switch, uma vez que a memória esteja cheia, o Switch não vai conseguir definir quem está onde e ele passa a atuar como um Hub.

Como podemos nos prevenir contra esse ataque?

- Configurar a opção de segurança na porta, para que assim fique limitada a receber uma quantidade máxima de endereços MAC, caso ultrapasse, a porta é desabilitada
- Podemos configurar a porta do Switch para aceitar um número máximo de endereços MAC, ao ultrapassar esse limite a porta é desligada e o ataque não teria sucesso.

# Aula 6

Qual a função da máscara de rede?

- Dividir o endereço IP em dois grupos (rede e máquina) e a partir daí poder definir quando outro dispositivo estará na mesma rede que eu.
- A máscara de rede é usada como forma de comparação para determinar se dois equipamentos estão na mesma rede. Para isso ela vai dividir o endereço IP em dois grupos, de rede e hosts (máquinas).

Esses dois dispositivos:

1- IP: 192.168.0.3 ; Máscara: 255.255.255.0

2- IP: 192.169.0.4 ; Máscara: 255.255.255.0

Estão na mesma rede?

- Não
- Lembre-se, a máscara de rede está dizendo que para dois equipamentos estarem na mesma rede, os 3 primeiros octetos do IP devem ser iguais, uma vez que suas máscaras são 255.255.255.0.

Se eu tenho um endereço IP: 33.44.55.66 e máscara de rede: 255.0.0.0, qual desses endereços abaixo vai caracterizar que outro dispositivo está na mesma rede que eu?

Lembre-se: - 255 = Rede - 0 = Host

- IP: 33.255.4.3 ; Máscara: 255.0.0.0
- O 1° octeto do endereço IP é 33, logo só ele me importa para analisar se outro dispositivo está na mesma rede que eu, os demais são números da máquina. As outras opções começam com número diferente de 33, o que caracteriza que a máquina está em outra rede.

Qual equipamento é usado para comunicar com redes externas?

- Roteador
- A função do roteador é interconectar redes encaminhando seus pacotes de dados, os Switches e hubs são usados somente para conexão na minha rede local.

Para conectar um computador com um roteador, qual tipo de cabo eu uso?

- Cabo cruzado
- Lembre-se da regra: - Dois equipamentos iguais estão interconectados? Se sim, eles tem o mesmo tipo de placa, então devo usar o cabo crossover. Se não, faço a pergunta abaixo - Dois equipamentos diferentes estão conectados? Essa conexão representa o que naturalmente o equipamento foi desenvolvido para fazer? Por exemplo ao interconectar o computador ao hub e o computador ao switch, o computador foi feito para se comunicar com várias máquinas e o hub e switch foram feitos para interconectar diversas máquinas. Dessa forma ao conectarmos os dois, vamos estar explorando o que os dois foram fabricados para fazer naturalmente. Porém o roteador foi feito para interconectar redes, se eu coloco somente um dispositivo, não terei como inserir outros dispositivos para o roteador encaminhar os pacotes e então a totalidade de sua função não está sendo explora. Devemos usar cabo crossover.

Para que serve o default gateway?

- Ele é a "porta de saída" da minha rede
- O default gateway é o endereço IP o qual será responsável por encaminhar pacotes para redes externas, é o IP do meu roteador.

# Aula 7

Quais são as classes de endereços IP que podem ser endereçadas para máquinas?

- Classe A, B e C
```
A IETF (Internet Engineering Task Force) determinou que existiriam ao todo 5 classes de endereços IP, indo de ordem alfabética da classe A até a classe E. Porém as duas últimas classes não são usadas para serem endereçadas as máquinas. A classe D seria usada para multicast (termo usado quando queremos nos comunicar com somente algumas máquinas de nossa rede) e a classe E seria uma classe experimental. Portanto as classes de IP que podem ser endereçadas para máquinas seriam a classe A, B e C.
```

Como eu identifico que um endereço IP está em uma classe?

- Pelo valor do primeiro intervalo (octeto)
```
Para sabermos em qual classe um endereço IP se encontra, temos que analisar o primeiro octeto e ver dentro de qual range ele estaria. (Classe A, B ou C).
```

O endereço IP 187.77.45.8 estaria dentro de qual classe, considerando que usa máscara de rede padrão?

- Classe B
```
A classe "A" possui o primeiro octeto variando de 1 a 127, a classe "B" possui o primeiro octeto variando de 128 a 191 e a classe "C" possui o primeiro octeto variando de 192 a 223. Dessa forma pelo fato do número 187 se encontrar dentro de 128 a 191, sabemos que é um endereço da classe "B".
```

O que seria o endereço 127.0.0.1? Como ele é conhecido?

- É um endereço __interno da placa de rede__, usado para testar se os protocolos TCP/IP estão funcionando. Ele é conhecido como __endereço de loopback__, pois o sinal é enviado e recebido por ele mesmo.
```
O endereço 127.0.0.1 seria uma faixa de endereço IP reservada, esse seria um endereço interno da placa de rede para realizar testes e verificar se ela está de fato validando os protocolos TCP/IP.
```

O que são IPs privados?

- São IPs que são usados somente para comunicação na rede local, não posso acessar a internet
```
Os endereços IP privados são usados para comunicação somente em minha rede local, de acordo com a especificação, eles não podem ser usados para comunicação na internet por exemplo.
```

Se eu tenho IP privado na minha máquina, como posso acessar a internet?

- Através do método de tradução de endereços IPs privados para públicos, chamado de NAT
```
Isso acontece porque nosso roteador possui a configuração chamada NAT, essa configuração vai converter o endereço IP privado que temos em nossas máquinas para IP públicos que nosso provedor de serviços nos fornece.
```

Qual foi a evolução do IPv4?

- IPv6
```
A evolução do IPv4 seria a versão 6 do protocolo, que seria conhecida como IPv6.
```

Por que foi necessário o IPv6?

- Porque os endereços públicos do IPv4 se esgotaram
```
O endereço IPv6 foi necessário porque os endereços IPv4 públicos chegaram a um fim por conta da grande popularidade da internet, smartphones, tablets, etc.
```

Dado que o endereço IP da máquina 7.8.7.8 possui máscara de rede 255.0.0.0, determine seu endereço de rede e broadcast (Lembre-se da regra, endereço de rede e broadcast):

- Rede: 7.0.0.0; Broadcast: 7.255.255.255
```
Descobrir endereço de rede que esse endereço IP está inserido:

Se recortarmos o 255 da máscara de rede e inserirmos o octeto correspondente do endereço IP, teremos: 7.0.0.0 :)
Descobrir o endereço de broadcast da rede:

Pegamos o endereço de rede e recortamos os 0’s (originais da máscara) e colocamos 255 no lugar, teremos então: 7.255.255.255
Dessa forma, por exemplo o endereço IP: 7.0.0.255 é válido porque é maior que o endereço de rede (7.0.0.0) e menor que o de broadcast (7.255.255.255)
```

Dado que o endereço IP da máquina 135.44.3.21 possui máscara de rede 255.255.0.0, determine seu endereço de rede e broadcast (Lembre-se da regra, endereço de rede e broadcast):

- Rede: 135.44.0.0; Broadcastr: 135.44.255.255
```
Descobrir endereço de rede que esse endereço IP está inserido:

Se recortarmos o 255 da máscara de rede e inserirmos os octetos correspondentes do endereço IP, teremos: 135.44.0.0
Descobrir o endereço de broadcast da rede:

Pegamos o endereço de rede e recortamos os 0’s (originais da máscara) e colocamos 255 no lugar, teremos então: 135.44.255.255
Dessa forma, por exemplo o endereço IP: 135.44.0.255 é válido por que é maior que o endereço de rede (135.44.0.0) e menor que o de broadcast (135.44.255.255)
```

O que caracteriza uma comunicação broadcast?

- Comunicação com todos os dispositivos da minha rede
```
Broadcast seria um termo usado quando a comunicação é feita para todos os dispositivos que estão na mesma rede.
```

# Aula 8

Para que serve um servidor DHCP?

- Para atribuir IP a máquinas (clientes) de forma dinânima
```
Os servidores DHCP (Dynamic Host Configuration Protocol) alocam dinamicamente endereços IPs a clientes (máquinas).
```

Como é conhecida essa forma de atribuição de IP pelo DHCP?

- IP dinâmico
```
Quando um endereço IP é atribuído a uma máquina (cliente), dizemos que a configuração foi dinamicamente alocado. Os servidores DHCP normalmente possuem o que chamamos de “lease time”, ou seja possui um tempo de alocação de um endereço IP a uma máquina, quando esse tempo é expirado é preciso ocorrer uma renovação de endereço IP. Por isso ele é dinamicamente alocado :)
```

Quando um cliente não possui um endereço IP e está configurado para receber IP dinâmico, como ele faz a requisição para que alguém forneça um endereço IP?

- Broadcast
```
Quando um cliente não possui endereço IP ele não sabe a quem perguntar, então ele precisa sair perguntando para todo mundo que está na mesma rede quem poderá fornecer um endereço IP. Quando essa comunicação é feita para todos os dispositivos, chamamos isso de Broadcast.
```