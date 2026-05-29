# Documentação Bloco A

---

A equipe de TI fica alocada no Bloco A da empresa. Três subequipes estão representadas neste laboratório:
- Equipe de Rede  
- Equipe de Analistas  
- Equipe do Call Center  

---

## Segmentação da Rede

- Cada subequipe está conectada a um switch Cisco 2960 dedicado, com a seguinte organização.
- Cada switch terá uma conexão trunk com o switch da camada de distribuição.

## Padrão de configuração dos switches de acesso
- Portas FastEthernet 0/1 a 0/24 configuradas como acesso
- Apenas as portas FastEthernet 0/1 a 0/3 estarão ativas para conexão dos PCs
- Demais portas permanecerão em shutdown (administrativamente down)
- Porta GigabitEthernet 0/1 configurada como trunk para o switch 3650 (camada de distribuição)
- Porta GigabitEthernet 0/2 em shutdown, reservada para redundância futura


## Definição das VLANs
Equipe de Rede:
- VLAN 100 - 172.16.100.0/24

Equipe de Analistas:
- VLAN 110 - 172.16.110.0/24

Equipe de Call Center::
- VLAN 120 - 172.16.120.0/24


**Nota:** As interfaces trunk devem permitir apenas as VLANs necessárias para a operação da equipe

---

### Equipamentos Bloco A

- 1 Switch 3650 24PS GigabitEthernet - switch de camada de distribuição (Layer 3)  
- 3 Switches 2960 24TT - switches de camada de acesso (Layer 2)  
- 9 Desktops - dispositivos de usuário final  

---

## Observações

- Cada equipe utiliza um switch de acesso dedicado  
- As VLANs garantem o isolamento lógico entre as subequipes  
- O ambiente está preparado para futura implementação de roteamento entre VLANs  
- Este laboratório representa a estrutura lógica da equipe de TI no Bloco A

---

## Camada de distribuição
A camada de distribuição do bloco A acomoda um switche 3650 24PS GigabitEthernet (Layer 3) que proverá o roteamento entre VLANs e o roteamento externo.

---
## Padrão de endereçamento – Camada de Distribuição
O último endereço IPv4 válido de cada sub-rede será utilizado como gateway das VLANs configurando o na (interface VLAN – SVI) nesta fase inicial.
Em versões futuras, com a implementação de redundância (HSRP), será adotado o seguinte padrão:
- Endereço virtual (gateway) → último IP da sub-rede (.254)
- Switch primário → primeiro IP válido (.1)
- Switch secundário → segundo IP válido (.2)

**Nota** Essa abordagem garante que não será necessário alterar o gateway configurado nos hosts durante a implementação da redundância

