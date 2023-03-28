#Crie o arquivo dentro de .docker/apache
FROM httpd:2.4
#copy angular dist folder to container 
COPY dist/html /usr/local/apache2/htdocs/

#copy htaccess and httpd.conf to container
COPY .htaccess /usr/local/apache2/htdocs/
COPY httpd.conf /usr/local/apache2/conf/httpd.conf
#change permissions
RUN chmod -R 755 /usr/local/apache2/htdocs/

#expose port
EXPOSE 4200


#Após isso, rode os seguintes comandos:
#docker build -f ./.docker/apache/Dockerfile -t nomedasuaapp .
#docker run -p 4200:4200 nomedasuaapp
