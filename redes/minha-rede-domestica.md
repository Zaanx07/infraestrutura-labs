# Minha Rede Doméstica

## Objetivo

Analisar a configuração da minha rede doméstica e compreender como os dispositivos se comunicam com a Internet.

---

## Informações da Rede

### Nome do Computador

LAB-WIN11

### Endereço IPv4

10.100.83.xxx

### Gateway Padrão

10.100.95.254

### Servidor DNS

10.100.198.1

10.100.198.2

### Servidor DHCP

10.100.198.2

---

## Análise Inicial

As informações foram coletadas em uma máquina virtual de laboratório utilizada para fins de estudo.

Foi identificado que o equipamento recebeu automaticamente um endereço IPv4 pertencente à faixa privada 10.x.x.x através de um servidor DHCP.

O gateway padrão configurado é responsável por encaminhar o tráfego para outras redes e permitir o acesso a recursos externos.

A resolução de nomes é realizada por servidores DNS internos, responsáveis por converter nomes de domínio em endereços IP.

A utilização de servidores dedicados para DHCP e DNS é uma prática comum em ambientes corporativos, pois permite centralizar o gerenciamento dos serviços de rede.

> Observação: Alguns dados foram mascarados ou adaptados para preservar informações internas do ambiente analisado.

## Testes de Conectividade

### Ping para google.com

Foi realizado um teste de conectividade utilizando o domínio google.com.

**Resultado observado:**

* 4 pacotes enviados
* 4 pacotes recebidos
* 0% de perda de pacotes
* Tempo médio de resposta: 21 ms

**Análise:**

O teste foi concluído com sucesso, demonstrando que o equipamento possui acesso à Internet e consegue se comunicar corretamente com servidores externos através da resolução de nomes realizada pelo DNS.

---

### Ping para 8.8.8.8

Foi realizado um teste de conectividade utilizando o endereço IP público 8.8.8.8 (Google DNS).

**Resultado observado:**

* 4 pacotes enviados
* 4 pacotes recebidos
* 0% de perda de pacotes
* Tempo médio de resposta: 10 ms

**Análise:**

O teste confirmou que existe conectividade IP com a Internet. Como o acesso foi realizado diretamente através do endereço IP, não houve necessidade de resolução de nomes por DNS.

---

## Teste de Resolução de Nomes

### nslookup google.com

Foi realizado um teste utilizando a ferramenta nslookup para verificar o funcionamento do serviço DNS.

**Resultado observado:**

Servidor DNS utilizado:

* 10.100.198.1

Domínio consultado:

* google.com

Endereços retornados:

* 172.217.30.46
* 2800:3f0:4001:83b::200e

**Análise:**

O servidor DNS respondeu corretamente à consulta e converteu o nome de domínio google.com para seus respectivos endereços IP.

O resultado demonstra que a resolução de nomes está funcionando adequadamente, permitindo que aplicações e navegadores localizem serviços na Internet utilizando nomes amigáveis em vez de endereços IP numéricos.

---

## Conclusão

Durante este laboratório foi possível analisar a configuração básica de rede do equipamento e validar os principais serviços necessários para comunicação com a Internet.

Os testes realizados confirmaram o funcionamento adequado do endereçamento IP, gateway padrão, DHCP, DNS e conectividade externa.

Além disso, foi possível observar na prática como ocorre a resolução de nomes através do DNS e como os dispositivos utilizam endereços IP para estabelecer comunicação com recursos externos.