Neste projeto, realizei a conexão entre duas VPCs utilizando o VPC Peering.

Criação das VPCs:

1 - Duas VPCs foram criadas na mesma região, cada uma com seu próprio CIDR block (10.0.0.0/16 e 10.1.0.0/16).

Subnets públicas distintas foram criadas em Availability Zones diferentes.

2 - Instâncias EC2:

Foram lançadas duas instâncias EC2, uma em cada subnet pública.

As instâncias foram configuradas com acesso SSH utilizando uma Key Pair válida.

3 - Criação do VPC Peering:

Foi criado um VPC Peering entre as duas VPCs.

O peering foi aceito e ativado manualmente.

4 - Tabelas de Roteamento:

As rotas foram adicionadas nas tabelas de roteamento públicas, permitindo tráfego entre os CIDRs das duas VPCs.

5 - Configuração de Security Groups:

As regras dos SGs foram atualizadas para:

Permitir acesso SSH (porta 22) a partir da internet (0.0.0.0/0) para testes.

Permitir todo o tráfego interno entre as subnets envolvidas.

6 - Conexão e Testes:

As instâncias foram acessadas via SSH através do Git Bash.

A comunicação entre as duas VPCs foi validada com sucesso. As instâncias EC2 puderam se comunicar entre si mesmo estando em redes distintas, graças à configuração correta de peering, rotas e SGs.




Evidências

1 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/VPC-A.png
2 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/VPC-B.png
3 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/peering.png
4 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/route_table_VPC_A.png
5 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/route_table_VPC_B.png
6 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/EC2_A.png
7 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/EC2_B.png
8 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/SG_VPC_A.png
9 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/SG_VPC_B.png
10 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/Ping_A.png
11 - https://github.com/RobertoJanuario/VPC-Peering/blob/master/ping_B.png
