
### Curso Digital: Redes e Sistemas

#### Infraestrutura de redes e principais equipamentos:

* NIC - Network Interface Card: <br> 
Placa de rede como é mais conhecida, é o dispositivo responsável pelo acesso do computador à conexão através do cabo de rede Ethernet ou por receber ondas de rádio frequência das conexões wireless.

* HUB: <br>
O HUB é um hardware que permite a conexão entre dispositivos através de cabos de par trançados e conectados entre si.

* Switch: <br>
Responsável pela computação dos quadros entre os dispositivos, podemos definir a computação como troca ou encaminhamento de informação.

* Roteador: <br>
O roteador tem a responsabilidade de procurar as melhores rotas na internet para entregar os pacotes do remetente ao destinatário no menor tempo possivel.

* Modem: <br>
É o equipamento responsável pela modulação e demodulação do sinal de internet.

* Rack: <br>
 O rack é um armário para hospedar os equipamentos de hardwares como switchers, roteadores, modens, fibras ópticas e organizar os cabos em patch panels. Ele é essencial em data centers e infraestrutura de redes.

---

## Cabeamento estruturado 

* São padrões estabelecidos que definem como serão as organizações dos cabos e seus periféricos possibilitando melhor organização e performance de rede.

##### Normas: 
    -> NBR 14.565
    -> ANSI/TIA 568
    -> ANSI/TIA 569

* Cabo de par trançado:<br>
Eles são divididos em categorias que determinam     a velocidade de transmissão dos dados e o alcance em metros que o cabo deve suportar sem a perda de pacotes. 
O cabo é de cobre e dividido em oito fios, cada fio tendo uma funcionalidade.
Há dois tipos de cabo, o UTP e STP. 
##### Cabo UTP - Não possui isolamento, os fios são ligados diretamente entre si. O ponto negativo é a falta de isolamento, oferecendo ruidos, interferências... 
##### Cabo STP - Tem a função de cobrir as deficiências do UTP, permitindo isolamento. 

* Cabo Coaxial: <br>
É composto por fios de cobre, tendo um fio central responsável por ser o condutor do pulso elétrico, malha metálica realizando isolamento e uma blindagem plástica contra interferências externas. 

* Fibra Óptica: <br>
É a tecnologia guiada por cabo que oferece a maior velocidade de transmissão de dados chegando a altas velocidades na casa dos Gbps. A fibra é composta por pedaços de vidros que permitem a propagação dos raios de luz que são convertidos por conversores nas extremidades das fibras.  

---
## Modelo OSI e TCP/IP 

* A diferença entre o modelo OSI e o TCP/IP é que o modelo OSI é uma padronização, um modelo conceitual que serve de base para criar outros modelos, e o modelo TCP/IP temos implementado na prática, combinando algumas camadas do OSI em uma só.


### Modelo OSI 

* Aplicação - Contém as informações do browser, protocolos DNS, protocolos SSH. 
* Apresentação - Criptografia, conexão segura, evitar vazamento de dados. 
* Sessão - Responsável por estabelecer uma sessão entre a origem e seu destino final. 

As camadas acima são as mais próximas do usuário, o que ele "consegue manipular".
Já as camadas abaixo ficam por parte do hardware, computadores, roteadores, switchers fazem a comunicação entre si e passar para cima ou baixo na tabela.

* Transporte - Realiza a conexão através de dois protocolos: protocolo TCP e o protocolo UDP.
* protocolo TCP - Envia um dado para o destino final, o dado é chamado de "segmento", contendo informações sobre o que está sendo enviado, para onde será enviado, de onde está sendo enviado. Ao enviar o segmento para o destino, o protocolo TCP pede a confirmação de que os dados chegaram corretamente, havendo uma verificação e se tiver algum erro, irá reenviar o segmento. 
* protocolo UDP - Irá enviar o segmento mas não há verificação se os dados chegaram corretamente no destino. Caso ocorra um erro, ele não reenvia.  
* Rede - É onde ocorre os envios de dados, o modelo osi ao passar os dados para a rede, ele deixa de ser segmento e se torna um pacote que será mandado para um roteador. 
* Enlace - Responsável por pegar o endereço MAC, fazendo a utiliazação para realizar o envio de dados, mensagens, buscando pelo MAC address do destino final para enviar a mensagem.
* Física - O cabo, o roteador, qualquer periférico que tenha a conexão. Há protocolos para ocorrer a comunicação nessa camada, um exemplo o Ethernet, determinando latência, velocidade, etc. 

### Modelo TCP/IP 
#### O modelo TCP/IP, diferente do modelo OSI que é dividido em sete camadas, contém apenas quatro; "Aplicação, Transporte, Internet, Acesso a Rede."
### Exemplo abaixo da diferença entre os modelos TCP/IP e OSI:

<img src="src/osi-tcp-ip.png">

---

## IPV4 e IPV6

* IP - Internet Protocol. <br> 
    O termo IP (Internet Protocol) é o protocolo responsável pelo endereçamento dos pacotes de rede na camada 3 do modelo OSI, ou seja, o responsável por gerar um endereço ao seu computador, ou qualquer servidor, no momento que este conecta-se à internet. Atualmente existem dois formatos: IPV4 e IPV6. 

#### IPV4: 192.168.0.1
##### Formato de 32 bits dividido em 8 ectetos onde cada ecteto pode variar de 0 até 255. O IPV4 permitia aproximadamente 4 bilhões de conexões, pois, os criadores na década de 80 acharam que não teria tantas pessoas no mundo, mas atualmente o número praticamente dobrou, e para resolver esse problema, há uma solução que é o famoso ip público, e isso significa que uma casa pode ter mais de 50 dispositivos conectados à internet, mas todos usarão o mesmo ip para ter conexão. 

#### IPV6: 1050:0000:0000:0000:0005:0600:300c:326b(11050:0:0:0:5:600:300c:326b)
##### Formato de 128 bits dividido em 16 pares. Já o IPV6 permite mais de 340 decilhões de conexões.

---

## Calculo de sub rede

### Classes de endereço IP: 
<img src=src/redes1.jpg>

---

## Domínios, DNS e Latência

### Domínio Raiz: 
<img src=src/dns-root-server.jpg>

* O domínio raiz é o topo da hierarquia de domínios, contendo muitos subdomínios. Pode ser adquirido com um nome específico para a empresa ou uso pessoal. A estrutura do domínio afeta a classificação do site.

### Domínio e Subdomínio:
<img src=src/componentes-url-com-subdominio.png>

* Domínio é o nome de identificação de um site na internet, por exemplo, resultadosdigitais.com.br. Subdomínio é um endereço que faz parte do domínio, ou seja, é uma ramificação do domínio. Subdiretório é um diretório ou pasta criado a partir do site principal. 

### Latência:
<img src=src/latencia.png>

* Latência de rede é o atraso na comunicação da rede. Ela mostra o tempo que os dados demoram para serem transferidos pela rede.

---

## Principais comandos de configuração em redes de computadores

#### Exibir configurações de IP do windows
    ipconfig
#### Limpar o cache DNS de sua máquina
    ipconfig /flushdns
#### Testar a conexão de sua máquina com outro host
    ping google.com
#### Obter informações sobre registro DNS de um domínio, host ou ip
    nslookup
#### Mapear requisição da origem ao host, domínio ou ip
    tracert google.com
#### Exibir tabela de roteamento do host
    route print
#### Mapear quais portas estão sendo usadas no computador
    netstat
