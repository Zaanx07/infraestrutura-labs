# Fundamentos de Redes

## Objetivo

Describir los conceptos básicos de redes que sirven como base para la comunicación entre dispositivos en ambientes domésticos y corporativos.

---

## O que é uma rede?

É um conjunto de dispositivos interconectados que podem compartilhar dados, recursos e serviços. Esses dispositivos podem ser conhecidos como nós e podem ser computadores, servidores, dispositivos móveis, impressoras ou qualquer dispositivo capaz de enviar e receber dados.

### Componentes-chave de uma rede

#### Nós (Dispositivos)

São os pontos de terminação da rede, podendo ser usuários finais, servidores, dispositivos de rede, entre outros.

#### Meios de transmissão

São os meios físicos ou sem fio através dos quais os dados são transmitidos, como cabos de cobre, fibra óptica e redes sem fio.

#### Dispositivos de rede

Equipamentos como roteadores, switches e pontos de acesso que facilitam o tráfego de dados entre os dispositivos conectados.

#### Protocolos

São conjuntos de regras e padrões que definem como os dispositivos se comunicam dentro da rede, como TCP/IP, HTTP e FTP.

---

## Tipos de Rede

### LAN (Local Area Network)

É uma rede de computadores que conecta dispositivos dentro de uma área geográfica limitada, como uma residência, escritório ou edifício.

### Exemplo de LAN

- Rede doméstica
- Rede de um escritório
- Rede de uma escola

### WAN (Wide Area Network)

É uma rede de longa distância que conecta múltiplas redes locais (LANs) através de grandes áreas geográficas, como cidades, países ou continentes. É utilizada tanto em infraestruturas públicas quanto privadas.

### Exemplo de WAN

- Internet
- Rede corporativa entre filiais de uma empresa

## Comparação entre LAN e WAN

| Característica | LAN | WAN |
|---------------|-----|-----|
| Alcance | Área limitada | Grandes distâncias |
| Exemplo | Casa, escritório | Internet, filiais |
| Velocidade | Geralmente maior | Pode variar |

---

## Principais Componentes de uma Rede

### Computador / Host

É o dispositivo final da rede que envia e recebe dados. Pode ser um computador, impressora, celular ou qualquer outro dispositivo conectado à rede. Possui um endereço IP para ser identificado na comunicação com outros dispositivos.

### Switch

É um dispositivo que conecta múltiplos equipamentos dentro de uma rede local (LAN) e encaminha os dados apenas para o destinatário correto. Trabalha principalmente com endereços MAC.

### Roteador (Router)

É um dispositivo que conecta diferentes redes entre si e direciona o tráfego de dados entre elas. Utiliza endereços IP para encaminhar as informações e possibilita o acesso à Internet.

### Modem

É o dispositivo responsável por converter sinais digitais em analógicos (e vice-versa), permitindo a conexão com a Internet através do provedor de serviços (ISP). É utilizado em conexões de cabo, DSL ou fibra óptica.

### Servidor

É o equipamento responsável por fornecer serviços, recursos ou informações para outros dispositivos conectados à rede.

---

## Endereço IP

### O que é um endereço IP?

É um endereço lógico utilizado para identificar um dispositivo em uma rede e permitir a comunicação entre equipamentos.

### IP Público

É o endereço IP único que identifica um dispositivo ou rede na Internet. Pode ser acessado pela Internet, é atribuído pelo provedor de serviços (ISP) e deve ser único em nível mundial.

**Analogia:** É como o endereço da sua casa dentro de uma cidade.

### IP Privado

É o endereço IP utilizado dentro de uma rede local (LAN) para identificar dispositivos internamente. Não é acessível diretamente pela Internet, pode ser reutilizado em diferentes redes e geralmente é atribuído por um roteador ou servidor DHCP.

**Analogia:** É como o número de um apartamento ou sala dentro de um edifício.

---

## MAC

Os endereços MAC (Media Access Control) são identificadores de 48 bits atribuídos às interfaces de rede. Também são conhecidos como endereços físicos e são representados em formato hexadecimal.

Esses endereços são utilizados para identificar dispositivos em uma comunicação dentro da rede local.

---

## Gateway

É o dispositivo ou endereço responsável por permitir a saída de uma rede local para outras redes ou para a Internet.

Normalmente, o gateway corresponde ao endereço IP do roteador da rede.

---

## DNS

DNS (Domain Name System) é o sistema responsável por traduzir nomes de domínio, como `google.com`, em endereços IP.

Isso evita a necessidade de memorizar endereços IP para acessar sites e serviços na Internet.

---

## DHCP

DHCP (Dynamic Host Configuration Protocol) é o protocolo responsável por atribuir automaticamente endereços IP e outros parâmetros de rede aos dispositivos conectados.

Entre as configurações fornecidas pelo DHCP estão:

* Endereço IP
* Gateway padrão
* Servidores DNS

Isso evita a necessidade de configurar manualmente os parâmetros de rede em cada dispositivo.

---

## Conclusão

Durante este estudo, foi possível compreender os conceitos básicos que permitem a comunicação entre dispositivos em uma rede, incluindo endereçamento IP, identificação por MAC, resolução de nomes através do DNS e atribuição automática de configurações por meio do DHCP.

Esses conceitos servirão como base para os próximos estudos relacionados a Windows Server, Active Directory, infraestrutura de redes e computação em nuvem.

