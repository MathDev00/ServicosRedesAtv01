
                                                  ---------DOCUMENTAÇÃO ---------




a) Fornecer os arquivos de configuração necessários para cada serviço (DHCP, DNS, Firewall) e explicar suas escolhas 

Na seção 1. Arquivos segue em anexo no repostitório. 

A) dhcpd.conf


```
subnet 172.17.0.0 netmask 255.255.0.0 {
    range 172.17.0.10 172.17.0.100;
    option routers 172.17.0.10;
    option subnet-mask 255.255.0.0;
    option broadcast-address 172.17.255.255;
    default-lease-time 10;
    max-lease-time 10;
}

subnet 192.168.0.0 netmask 255.255.255.0 {
  range 192.168.0.100 192.168.0.200;
  option routers 192.168.0.1;
  option domain-name-servers 8.8.8.8;
  option domain-name "example.com";
}
```

Observação: 


A) named.conf




Documentar todo o processo de configuração e os resultados dos testes realizados.
Recomenda-se o uso de volumes Docker para persistência de dados, quando necessário.
Os participantes devem estar preparados para responder a perguntas sobre suas escolhas de configuração e solução de problemas durante a apresentação do exercício, que será agendada posteriormente.





1. Introdução aos serviços

O projeto visa a criação e implementação de serviços utilizando o Docker. O Docker é uma ferramenta que facilita a criação de contêineres. Os contêineres garantem  isolamento dos serviços, tornando a implantação mais eficiente. 

| SERVIÇOS | DESC |
| ------------- | ------------- |
| DHCP | Configura um servidor DHCP em um ambiente Linux para atribuir automaticamente endereços IP aos dispositivos na rede. O DHCP simplifica a administração da rede, fornecendo configuração dinâmica de endereços IP, gateway padrão, máscara de sub-rede, servidor DNS, entre outros parâmetros de rede. |
| DNS  |Implanta um servidor DNS para resolver nomes de domínio dentro da rede.  |
| Firewall| O firewall é uma medida de segurança essencial para proteger os recursos da rede contra acessos não autorizados. Através do firewall, é possível controlar o tráfego de entrada e saída, permitindo apenas o acesso aos serviços necessários e bloqueando tentativas de acesso malicioso. Considerando a própria tradução literal da palavra do português ao inglês, é uma parede de fogo, que bloqueia acesso definidos em arquivos do serviço.|


2. Testes

2.1 Testes com DHCP

 - Executando o containers
 - Testando funcionamento do serviço. Serviço DHCP foi iniciado, de acordo com a informação abaixo.


  ![Texto Alternativo](dhcp.png)

   - Testando atribuição DHCP no servidor DNS, com IP e nome de rede (de acordo com o arquivo de configuração)

       ![Texto Alternativo](dns2.png)



  3.2 Testes com DNS

 - Executando o containers

  ![Texto Alternativo](dns.png)


  - Testando atribuição nomes de redes com ping

  ![Texto Alternativo](dns3.png)

  3.3 Testes com Firewall

 - Executando o containers

  ![Texto Alternativo](dhcp.png)


  - Testando 

  ![Texto Alternativo](dhcp.png)








