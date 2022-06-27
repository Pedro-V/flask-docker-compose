# Counter App usando Docker Compose

O Docker Compose v2 foi reescrito em `go` e tem algumas funcionalidades a mais. Nesse repositório git eu só registrei o uso da ferramenta pra rodar:

* Um app muito simples usando `flask`
* Um backend rudimentar usando `redis`

O foco não é o frontend/backend, mas só a capacidade de rodar múltiplos containers de forma coordenada e *seamless* usando `docker`, que é um software que eu ainda estou aprendendo. 

## Rodando

Todo o repositório foi construído no Linux, usando a distro Ubuntu 20.04 (LTS). Eu não incluo aqui como rodar as aplicações nativamente no Windows.

O jeito mais tranquilo de rodar:

1. Clone esse repositório na sua máquina
        
        $ git clone https://github.com/Pedro-V/flask-docker-compose.git

2. Execute o docker compose. O `&` garante que o terminal será conservado para você e ainda assim irá receber output da build.

        $ docker compose up &

3. Após aparecer algo como `Debugger PIN: xxx-xxx-xxx`, Insira o seguinte num browser:

        localhost:5000

Por padrão do `docker-compose.yml`, as conexões serão no localhost:5000. Isso pode ser modificado no mesmo arquivo. Mas atenção que mudanças talvez só tomem efeito depois que você remover os volumes associados com esses containers e rodar novamente o docker compose.

## Referências

* *Docker Deep Dive, May 2020 - Nigel Poulton*

* docs.docker.com
