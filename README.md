# aula-2---sistemas-distribuidos
desafio de criar servidor e resposta
desafio final respostas
1. Principal problema da arquitetura atual
 R: Sobrecarga, o servidor pode ter problemas pra carregar e pode acabar caindo

2. O que acontece se o servidor falhar
 R: Indisponibilidade total, o sistema fica fora do ar, nao podendo ser utilizado

3. Adicionar mais servidores poderia ajudar? Por quê?
 R: Sim, distribuindo entre varios servidores pra nao sobrecarregar

4. Função de um balanceador de carga (Load Balancer)
 R: Distribuição de tráfego e alta disponibilidade: Ele atua como uma porta de entrada única que recebe as requisições dos alunos e as distribui entre os servidores disponíveis, além de monitorar a saúde das instâncias, redirecionando o tráfego caso algum servidor falhe.

5. Cliente-Servidor ou P2P? Justifique.
 R: Cliente-Servidor (com arquitetura distribuída/Web): É o modelo ideal porque o sistema acadêmico exige centralização, consistência de dados e controle de concorrencia, já o P2P é inadequado devido à falta de autoridade central para validação e riscos de segurança.

Nova Arquitetura Proposta
                  [ Clientes / Alunos ]
                            │
                            ▼
              [ Balanceador de Carga (Load Balancer) ]
               /            │            \
              /             │             \
             ▼              ▼              ▼
     [ Servidor 1 ]   [ Servidor 2 ]   [ Servidor 3 ]  
             \              │              /
              \             │             /
               ▼            ▼            ▼
                     Camada de Cache
                            │
                            ▼
              [ Banco de Dados Relacional  ]
            
