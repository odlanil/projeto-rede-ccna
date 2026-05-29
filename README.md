# Projeto de Rede – Nível CCNA

Com base nas competências de nível CCNA, este projeto foi desenvolvido considerando uma empresa de médio porte que mantém suas operações administrativas em três prédios distintos, classificados como **Bloco A, Bloco B e Bloco C**.

O ambiente de chão de fábrica não será representado nesta primeira fase do projeto, assim como a conectividade Wi-Fi, que será abordada em versões futuras.

---

**Nota:**  
O total de funcionários, bem como sua distribuição por departamento e função, não será considerado neste projeto. Como abordagem didática, todos os departamentos contarão com uma faixa de endereçamento IP capaz de acomodar até **254 endereços IP**.

---

## Projeto por bloco

- Cada bloco conterá um switch de camada 3 (Layer 3), operando na camada de distribuição  
- Cada bloco conterá três switches de camada 2 (Layer 2), sendo um por departamento  
- Em cada switch, três desktops serão conectados para representar os usuários  
- Cada departamento contará com uma impressora de rede  

---

## Projeto do Data Center (DC)

O Data Center (DC) será responsável pela conectividade entre os blocos e pela disponibilização dos recursos comuns à empresa.

A camada de distribuição do DC contará com os seguintes elementos:

- Um switch de camada 3 para interligação entre os blocos  
- Um switch de camada 2 para conexão dos servidores  
- Um servidor DNS  
- Um servidor DHCP IPv4  

---

## Plano de endereçamento IP por setor e VLAN (camada de acesso)

O plano de endereçamento IP prevê a segmentação de cada bloco em três sub-redes distintas, organizadas conforme as áreas funcionais.

---

### Bloco A

- VLAN 100 – 172.16.100.0/24 – Equipe de Redes  
- VLAN 110 – 172.16.110.0/24 – Equipe de Suporte  
- VLAN 120 – 172.16.120.0/24 – Call Center  

---

### Bloco B

- VLAN 130 – 172.17.130.0/24 – Recursos Humanos  
- VLAN 140 – 172.17.140.0/24 – Financeiro  
- VLAN 150 – 172.17.150.0/24 – Jurídico  

---

### Bloco C

- VLAN 160 – 172.18.160.0/24 – Marketing  
- VLAN 170 – 172.18.170.0/24 – Compras  
- VLAN 180 – 172.18.180.0/24 – Vendas

  A topologia utilizada nesta primeira fase do projeto será a apresentada abaixo:
  <img width="1220" height="512" alt="Topologia" src="https://github.com/user-attachments/assets/77a0e190-060a-4782-a7c4-2b14330942d7" />


