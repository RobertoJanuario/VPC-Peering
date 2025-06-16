Neste projeto, realizei a conexão entre duas VPCs utilizando o VPC Peering.

1 - Foram criadas duas VPCs dentro da mesma região, com subnets em diferentes AZs.
2 - Foram criadas duas intâncias EC2, uma em cada subnet pública das VPCs.
3 - Foi criado o VPC Peering, pareando ambas as VPCs.
4 - Os CIDRs das VPCs foram adicionados nas tabelas de roteamento pública uma da outra.
5 - Os Security Group's foram configurados para permitir acesso SSH de qualquer endereço da internet e todo tráfego vindo dos IPs das subnets criadas.
6 - Me conectei nas instâncias via SSH através do Git Bash.
7 - utilizei o comando ping para testar a comunicação entre as instâncias.


Evidências

1 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/VPC-A.png
2 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/VPC-B.png
3 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/peering.png
4 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/root_table_VPC_A.png
5 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/root_table_VPC_B.png
6 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/EC2_A.png
7 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/EC2_B.png
8 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/SG_VPC_A.png
9 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/SG_VPC_B.png
10 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/Ping_A.png
11 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/ping_B.png
