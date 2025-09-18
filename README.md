<p align="center">
<img src="https://www.docker.com/wp-content/uploads/2022/03/horizontal-logo-monochromatic-white.png" width="50%">
</p>
<p align="center">
  Nesse repositório você encontrará <strong>comandos úteis</strong>, <strong>arquivos dockerfile</strong>, <strong>arquivos docker-compose</strong>
</p>

<h2> 📘 Comandos Úteis</h2>

<table>
  <thead>
    <tr>
      <th>Comando</th>
      <th>Descrição</th>  
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong>docker-compose up</strong>
      </td>
      <td>
        Para subir o seu projeto utilize esse comando.
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker-compose build --no-cache</strong>
      </td>
      <td>
        caso tenha atualizado alguma informação em seu arquivo dockerfile ou docker-compose, utilize esse comando para atualizar os container.
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker-compose down</strong>
      </td>
      <td>
        Para remover os container utilize esse comando.
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker-compose down --volumes</strong>
      </td>
      <td>
        Caso queira excluir os volumes
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker-compose exec <name_container> bash</strong>
      </td>
      <td>
        Caso queira executar algum comando dentro do container.
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker-compose -f docker-compose.test.yml up</strong>
      </td>
      <td>
        Caso queira executar um docker-compose com nome personalizado
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker network create <network_name> --subnet=10.11.0.0/16</strong>
      </td>
      <td>
        Criar uma nova rede com IP fixo
      </td>
    </tr>
    <tr>
      <td>
        <strong>docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' NOME_DO_CONTAINER</strong>
      </td>
      <td>Utilizado para encontrar o IP do container</td>
    </tr>
    <tr>
      <td>
        <strong>docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Ports}}"</strong>
      </td>
      <td>Lista o nome dos container ativo</td>
    </tr>
  </tbody>
</table>

<h2> 📂 Arquivos Dockerfile</h2>
Alguns exemplos de arquivos Dockerfile personalizados. <br> <br>
🔹<a href="https://github.com/TiagoParente/docker/tree/main/Angular">Angular</a> <br>
🔹<a href="#" style="pointer-events: none">Laravel</a> <em>(Atualmente utilizo o Sail)</em> <br><br>

<h2> Sail </h2>
Caso precise criar um novo banco de dados no container gerado pelo sail, será necessário alterar as permissões, basta rodar os comandos abaixo:

```
sail exec mysql bash
mysql -u root -p
password: password
GRANT ALL PRIVILEGES ON *.* TO 'sail'@'%';
FLUSH PRIVILEGES;
EXIT;
exit
```
