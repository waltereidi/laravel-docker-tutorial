<h1>Tutorial Docker com laravel para windows</h1>

<p> Instale o docker </p>
</br>
<p> Crie os arquivos docker-compose.yml e Dockerfile </br>
adicione as configurações existentes deste tutorial apenas para estes dois arquivos 
<p>
</br>
<p> abra o terminal de comandos dentro do vs code , </br>
Certifique-se de ter instalado as extensões do docker </br>
agora execute os seguintes comandos : </br>
<strong>docker-compose build </strong> </br>
<strong>docker-compose up </strong> </br>
<p>Verifique o seu docker do windows , e o container do laravel-docker foi </br>
criado dentro das images . Certifique-se de existam 3 aplicativos instaldos dentro deste container </br>
<strong> Mysql , laravel-docker , docker-phpadmin. </strong>

<p> agora volte ao terminal de comandos do vs-code , abra um novo terminal. </br>
e execute o comando : </br>
<strong> docker exec -it laravel-docker bash </strong>
Agora voce estára dentro do container do docker, o laravel-docker é o nome da aplicação descrita na config.</br>
Instale o laravel dentro deste terminal como de costume : <strong>composer create-project laravel-app </strong> </br> 
Certifique-se de que o arquivo env. foi configurado corretamente : <strong> Senha root , usuario root , host: mysql</strong><br>
Isto mesmo , host : <strong>mysql</strong> , é o nome do host que foi dado ao docker-compose.yml durante a configuração</br>
Execute os comandos <strong>php artisan migrate</strong> e por fim <strong> php artisan serve --host 0.0.0.0 </strong> 
Se voce utilizou a mesma configuração deste repositório , pode acessar o laravel através de seu navegador no pc </br>
na porta <strong>9000 </strong> e o phpadmin na porta <strong>9001</strong> ,não se esqueça de rodar o serve com o --host 0.0.0.0 </br>
é essencial para o docker.
</br></br>

Dicas : na configuração de portas para os aplicativos o lado esquerdo é a porta de seu pc e a direita é a porta do docker.</br>
é possivel automatizar os comandos do docker atravéz do Makefile , deve-se criar uma lista comandos que serão executados </br>
"uma automatização para usos futuros."

<p>
