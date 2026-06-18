# IPv4 e Sub-redes

## Objetivo

Compreender o funcionamento do endereçamento IPv4, máscaras de rede e segmentação de redes.

---

## O que é IPv4?

O Protocolo de Internet versão 4 (IPv4) é a quarta versão do Protocolo de Internet e é responsável pelo sistema de endereçamento que permite a identificação e a comunicação entre dispositivos em uma rede.

Cada dispositivo conectado a uma rede recebe um endereço IP único dentro do seu contexto de comunicação, possibilitando o envio e o recebimento de dados entre diferentes equipamentos e redes.

### Exemplo

Dispositivo A: 192.168.1.10

Dispositivo B: 192.168.1.20

Para que esses dispositivos possam se comunicar, cada um deve possuir um endereço IP válido e pertencer à mesma rede ou utilizar um roteador para alcançar outras redes.

---

## Estrutura de um Endereço IPv4

Um endereço IPv4 é composto por **32 bits**, divididos em **4 octetos** de **8 bits** cada.

Sua representação mais comum é em formato decimal, separada por pontos:

```text
X.X.X.X
```

Onde:

* Cada **X** representa um **octeto**.
* Um endereço IPv4 possui **4 octetos**.
* Cada octeto pode assumir valores de **0 a 255**.

### Exemplo

```text
192.168.1.1
```

Neste exemplo:

* Primeiro octeto: **192**
* Segundo octeto: **168**
* Terceiro octeto: **1**
* Quarto octeto: **1**

### Representação Interna

Embora normalmente seja representado em números decimais, internamente um endereço IPv4 é armazenado em formato binário.

Cada octeto corresponde a **8 bits**, totalizando **32 bits**.

Exemplo:

```text
Endereço decimal:
192.168.1.1

Representação binária:
11000000.10101000.00000001.00000001
```

---

## Classes de Endereços IPv4

Historicamente, os endereços IPv4 foram divididos em classes para facilitar a organização e o dimensionamento das redes. Atualmente, a maior parte das implementações utiliza CIDR (Classless Inter-Domain Routing), porém o conhecimento das classes continua sendo importante para compreender os fundamentos do endereçamento IP.

### Classe A

* Faixa do primeiro octeto: **1 a 126**
* Destinada a redes de grande porte.
* Possui um grande número de endereços disponíveis para hosts.

**Exemplo:**

```text
10.100.83.15
```

---

### Classe B

* Faixa do primeiro octeto: **128 a 191**
* Indicada para redes de médio porte.
* Oferece um equilíbrio entre quantidade de redes e de hosts.

**Exemplo:**

```text
172.20.10.5
```

---

### Classe C

* Faixa do primeiro octeto: **192 a 223**
* Utilizada principalmente em redes de pequeno porte.
* É muito comum em redes domésticas e pequenos escritórios.

**Exemplo:**

```text
192.168.1.100
```

---

## Faixas Privadas Mais Utilizadas

Existem intervalos reservados para uso em redes privadas, que não são roteados diretamente pela Internet:

| Classe   | Faixa Privada                 | Exemplo       |
| -------- | ----------------------------- | ------------- |
| Classe A | 10.0.0.0 – 10.255.255.255     | 10.100.83.15  |
| Classe B | 172.16.0.0 – 172.31.255.255   | 172.20.10.5   |
| Classe C | 192.168.0.0 – 192.168.255.255 | 192.168.1.100 |

## Observação

Durante este estudo, foi possível identificar que o endereço IP utilizado no laboratório (`10.100.83.x`) pertence à faixa privada da Classe A, amplamente utilizada em ambientes corporativos.

---

## Endereços Públicos e Privados

Os endereços IPv4 podem ser classificados como **públicos** ou **privados**, dependendo do ambiente em que são utilizados e de sua acessibilidade pela Internet.

### Endereço IP Público

Um endereço IP público é um identificador único utilizado para permitir a comunicação de dispositivos ou redes pela Internet.

Esses endereços são atribuídos por provedores de serviços de Internet (ISP) ou por organizações responsáveis pela distribuição de endereços IP e devem ser únicos em nível mundial.

**Exemplo:**

```text
8.8.8.8
```

Neste caso, qualquer dispositivo conectado à Internet pode enviar tráfego para esse endereço, desde que as políticas de segurança permitam.

---

### Endereço IP Privado

Um endereço IP privado é utilizado exclusivamente dentro de redes locais (LANs) e não pode ser roteado diretamente pela Internet.

Esses endereços podem ser reutilizados em diferentes organizações ou residências, pois seu uso é restrito ao ambiente interno da rede.

Os principais intervalos reservados para redes privadas são:

* **10.0.0.0 – 10.255.255.255**
* **172.16.0.0 – 172.31.255.255**
* **192.168.0.0 – 192.168.255.255**

**Exemplo:**

```text
192.168.1.100
```

ou

```text
10.100.83.15
```

---

## Comparação entre IP Público e IP Privado

| Característica              | IP Público          | IP Privado                  |
| --------------------------- | ------------------- | --------------------------- |
| Acessível pela Internet     | Sim                 | Não                         |
| Deve ser único mundialmente | Sim                 | Não                         |
| Utilização                  | Comunicação externa | Comunicação interna         |
| Exemplos                    | 8.8.8.8             | 192.168.1.100, 10.100.83.15 |

---

## Observação

Durante os laboratórios realizados, foi possível identificar a utilização de um endereço da faixa `10.x.x.x`, que pertence ao intervalo de endereços privados. Esse tipo de configuração é comum em ambientes corporativos, onde os dispositivos se comunicam internamente e acessam a Internet por meio de roteadores e mecanismos como NAT (Network Address Translation).

---

## Máscara de Rede

A máscara de rede é um valor utilizado para determinar qual parte de um endereço IP identifica a **rede** e qual parte identifica o **host** (dispositivo) dentro dessa rede.

Ela permite que os equipamentos saibam se o destino da comunicação está na mesma rede local ou se o tráfego deve ser encaminhado para um roteador (gateway).

### Exemplo

Considere o seguinte endereço IP:

```text
IP: 192.168.1.25
Máscara: 255.255.255.0
```

Nesse caso:

* A parte **192.168.1** representa a rede.
* A parte **25** identifica o dispositivo (host) dentro dessa rede.

Outro equipamento com endereço `192.168.1.50` pertence à mesma rede local, enquanto um equipamento com endereço `192.168.2.10` pertence a uma rede diferente.

### Máscaras mais comuns

| Máscara       | Prefixo CIDR | Quantidade aproximada de hosts |
| ------------- | ------------ | -----------------------------: |
| 255.0.0.0     | /8           |             Mais de 16 milhões |
| 255.255.0.0   | /16          |                     Até 65.534 |
| 255.255.255.0 | /24          |                        Até 254 |

### Importância

Sem a máscara de rede, um dispositivo não conseguiria identificar corretamente os limites da sua rede local.

Esse conceito é fundamental para o funcionamento do roteamento, da comunicação entre dispositivos e da organização de redes corporativas.

---

## CIDR (Classless Inter-Domain Routing)

O CIDR é um método moderno de representação de redes que substituiu o antigo sistema baseado em classes (A, B e C). Em vez de depender apenas da classe do endereço IP, o CIDR utiliza um **prefixo** para indicar quantos bits pertencem à rede.

Esse prefixo é representado por uma barra seguida de um número.

### Exemplo

```text
192.168.1.10/24
```

Nesse caso:

* `192.168.1.10` é o endereço IP.
* `/24` indica que os primeiros **24 bits** identificam a rede.
* Os **8 bits restantes** são utilizados para identificar os hosts.

### Equivalência entre CIDR e Máscara de Rede

| Prefixo CIDR | Máscara de Rede |
| ------------ | --------------- |
| /8           | 255.0.0.0       |
| /16          | 255.255.0.0     |
| /24          | 255.255.255.0   |
| /25          | 255.255.255.128 |
| /26          | 255.255.255.192 |

---

## O que é uma Sub-rede?

Uma sub-rede (subnet) é uma divisão lógica de uma rede maior em redes menores. Ela é criada utilizando a máscara de rede para separar os dispositivos em diferentes segmentos.

O principal objetivo das sub-redes é organizar melhor a infraestrutura, reduzir o tráfego desnecessário e facilitar o gerenciamento e a segurança da rede.

### Exemplo

Considere uma empresa com os seguintes departamentos:

* Administração
* Financeiro
* Recursos Humanos
* Tecnologia da Informação (TI)

Em vez de colocar todos os computadores na mesma rede, é possível criar uma sub-rede para cada departamento.

```text
Administração → 192.168.10.0/24

Financeiro → 192.168.20.0/24

Recursos Humanos → 192.168.30.0/24

TI → 192.168.40.0/24
```

Dessa forma, os dispositivos ficam organizados em segmentos independentes, facilitando o controle da comunicação e a aplicação de políticas de segurança.

### Vantagens das Sub-redes

* Melhor organização da infraestrutura de rede.
* Redução do tráfego de broadcast.
* Maior segurança entre diferentes setores ou grupos de dispositivos.
* Facilidade para administrar grandes ambientes corporativos.
* Melhor aproveitamento dos endereços IP disponíveis.

---

## Exemplo Prático

Considere os seguintes dispositivos em uma rede local:

| Dispositivo  | Endereço IP  | Máscara de Rede     |
| ------------ | ------------ | ------------------- |
| Computador A | 192.168.1.10 | 255.255.255.0 (/24) |
| Computador B | 192.168.1.25 | 255.255.255.0 (/24) |
| Computador C | 192.168.2.15 | 255.255.255.0 (/24) |

Nesse cenário:

* Os computadores **A** e **B** pertencem à mesma sub-rede (`192.168.1.0/24`) e podem se comunicar diretamente.
* O computador **C** pertence à sub-rede `192.168.2.0/24`, diferente da utilizada pelos computadores A e B.
* Para que o computador A se comunique com o computador C, o tráfego deverá ser encaminhado pelo **gateway (roteador)**, responsável por conectar redes distintas.

Esse exemplo demonstra como o endereço IP e a máscara de rede trabalham em conjunto para identificar a rede e determinar a forma correta de comunicação entre os dispositivos.

---

## Conclusão

Durante este estudo, foi possível compreender a estrutura de um endereço IPv4, o conceito de classes de endereçamento, a diferença entre endereços públicos e privados, o funcionamento das máscaras de rede e o papel das sub-redes na organização da infraestrutura.

Também foi possível entender que a combinação entre endereço IP e máscara de rede permite identificar se um dispositivo pertence à mesma rede local ou se é necessário utilizar um gateway para alcançar outra rede.

Esses conhecimentos constituem uma base essencial para estudos mais avançados em administração de redes, Windows Server, Active Directory, serviços de infraestrutura e computação em nuvem.