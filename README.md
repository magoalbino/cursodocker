# cursodocker
Implementação do exemplo de sistema do curso Docker da Cod3r
Utilizando docker-compose com cada ambiente separado em sua própria imagem, e uma estrutura de proxy reverso para não precisar expor a porta do backend.
A aplicação simula o envio de emails, permitindo criar vários servidores 'workers' para o disparo de emails em paralelo.

## Inicialização

- docker-compose up -d
- localhost:80
- verificar a estutura do banco: docker-compose exec db psql -U postgres -f scripts/check.sql
- da mesma forma, verificar os dados do banco: docker-compose exec db psql -U postgres -d email_sender -c 'select * from emails'
