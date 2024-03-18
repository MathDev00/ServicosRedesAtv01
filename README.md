
                                                  ---------DOCUMENTAÇÃO ---------


1. Introdução aos serviços

O projeto visa a criação e implementação de serviços utilizando o Docker. O Docker é uma ferramenta que facilita a criação de contêineres. Os contêineres garantem  isolamento dos serviços, tornando a implantação mais eficiente. 

| SERVIÇOS | DESC |
| ------------- | ------------- |
| DHCP | Configura um servidor DHCP em um ambiente Linux para atribuir automaticamente endereços IP aos dispositivos na rede. O DHCP simplifica a administração da rede, fornecendo configuração dinâmica de endereços IP, gateway padrão, máscara de sub-rede, servidor DNS, entre outros parâmetros de rede. |
| DNS  |Implanta um servidor DNS para resolver nomes de domínio dentro da rede.  |
| Firewall| O firewall é uma medida de segurança essencial para proteger os recursos da rede contra acessos não autorizados. Através do firewall, é possível controlar o tráfego de entrada e saída, permitindo apenas o acesso aos serviços necessários e bloqueando tentativas de acesso malicioso. Considerando a própria tradução literal da palavra do português ao inglês, é uma parede de fogo, que bloqueia acesso definidos em arquivos do serviço.|


3. Testes

3.1 Testes com DHCP

 - Executando o containers
 - Testando funcionamento do serviço. Serviço DHCP foi iniciado, de acordo com a informação abaixo.

  ![Texto Alternativo](dhcp.png)


  - Testando atribuição de IP com o ifconfig

  ![Texto Alternativo](dhcp.png)

  3.2 Testes com DNS

 - Executando o containers

  ![Texto Alternativo](dhcp.png)


  - Testando atribuição nomes de redes com ping

  ![Texto Alternativo](dhcp.png)

  3.3 Testes com Firewall

 - Executando o containers

  ![Texto Alternativo](dhcp.png)


  - Testando 

  ![Texto Alternativo](dhcp.png)








