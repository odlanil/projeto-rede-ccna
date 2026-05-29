
# Projeto de Rede – Nível CCNA

Este projeto foi desenvolvido considerando uma empresa de médio porte que mantém suas operações administrativas em três prédios distintos, classificados como **Bloco A, Bloco B e Bloco C e um Data Center**.

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

## Topologia física

---
<img width="1220" height="512" alt="Topologia" src="https://github.com/user-attachments/assets/3d18aaf4-9cbb-4774-9ee9-138de8d1e33d" />

---

**Nota:** uma habilidade cobrada pela cisco é a de configurar um roteador como um servidor DHCP, por esse motivo o servidor DHCP nesta topologia é um router.

---




