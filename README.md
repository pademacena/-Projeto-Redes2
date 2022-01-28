# Projeto de Redes 2 - UFF -> Blockchain

## Ideia

O objetivo do nosso projeto foi implementar o conceito de blockchain e apontar a melhor solução para a sua implementação, levando em consideração Segurança, Desenvolvimento, Devops e Custo.

## Desenvolvimento do projeto

### Blockchain 

Desenvolvemos uma aplicação com o funcionamento similar a de uma blockchain, com todas as suas regras . Nela quando executada a primeira fez, é criado o bloco Genesys da nossa blockchain, após isso podemos criar novos blocos colocando qualquer informação que quisermos, além disso adicionamos a opção de validação dos blocos, onde percorremos todos os blocos conferindo a sua integridade. Criamos também uma rota de consulta, com ela podemos pesquisar o que quisermos em todos os blocos, trazendo informação por bloco.

### API 

Nossa API foi desenhado para ser um gateway para interagir com Micro serviços, cada micro serviço desenvolvido separadamente para executar uma função especifica, trazendo mais segurança na suas consultas e inserções, facilitando manutenção e analise de logs, para correção e levantamento de estatísticas.

### Rede

Optamos por utilizar o protocolo TCP para termos uma confiança maior e a certeza de que as requisições vão ser atendidas, para prevenir possíveis perdas que possam ocorrer no protocolo de UDP. A única parte da nossa aplicação que terá comunicação externa será a nossa API, por segurança definimos que seria melhor manter os micro serviços e a nossa blockchain com acesso apenas para o grupo de segurança de rede.

Para melhor implementação, em produção iremos gerar as imagens em docker ( api, micro serviços e blockchain) para facilitar na implementação dos servidores com Kubernetes.

### Monitoramento

Para monitoramento da solução, iremos utilizar Grafana para acompanhar efetividade dos nossos micro serviços e o Elasticsearch para podermos acompanhar os logs e erros que ocorram em todo o processo.


