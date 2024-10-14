<h2>1-Comproba que a tes a imaxe http</h2>
 
    Usamos o comando ( docker images ) para ver se temos a imaxe.
 
<h2>2-Crea un contenedor de nome 'asir_httpd'. Mapea o porto 80 do contenedor có 8080 da túa máquina. Utiliza bind mount para que o directorio do apache2 'htdocs' estea montado nun directorio da túa elección. Utiliza -v "$PWD"/htdocs:/usr/local/apache2/htdocs/</h2>

    Para estes pasos utilicei o comando ( docker run -d --name asir_httpd -p 8080:80 -v "$PWD"/htdocs:/usr/local/       apache2/htdocs/ httpd )

<h2>3-Mostra unha páxina html aloxada no apache2 dende o teu navegador.</h2>

    Utilicei unha paxina html que xa tiña.

<h2>4-Crea un contenedor 'asir_web1' que use este mesmo directorio para 'htdocs' e o puerto 8000</h2>

    ( docker run -d --name asir_web1 -p 8080:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd )

<h2>5-Crea outro contenedor 'asir_web2' có el mesmo directorio e otro puerto, como o 8090.</h2>

    ( docker run -d --name asir_web2 -p 8090:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd )

<h2>6-Comproba que los dous servidores mostran a mesma páxina</h2>

    Se na misma carpeta tes a paxina html cando no buscador web poñas localhost:8080 ou localhost:8090 mostrarase a paxina html

Fai a entrega describindo os pasos usados con comandos no readme dun proxecto público en git, adxunta no entregable o enlace
