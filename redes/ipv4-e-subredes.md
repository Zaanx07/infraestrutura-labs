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

Pendente.

---

## Máscara de Rede

Pendente.

---

## O que é uma Sub-rede?

Pendente.

---

## Exemplo Prático

Pendente.

---

## Conclusão

Pendente.