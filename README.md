### Requisitos

1. Instalar [Docker](https://www.docker.com/community-edition#/download) version **17.05+**
2. Instalar [Docker Compose](https://docs.docker.com/compose/install/) version **1.6.0+**
3. Clonar este repositorio

Arrancar los contenedores
```console
$ docker-compose build
```

```console
$ docker-compose up
```
En el caso que no quiere mostrar log del servidor que mostrara sus acciones con los contenedores puede usar:
```console
$ docker-compose up -d
```

Kibana se iniciara en segundos despues que el logstash y elasticsearch procesan los datos, se puede ver la pantala de Kibana en esta direccion [http://localhost:5601](http://localhost:5601) en su navegador.
Por defecto, estos son los puertos de los contenedores pueston en marcha:
* 5000: Logstash TCP input.
* 9200: Elasticsearch HTTP
* 9300: Elasticsearch TCP transport
* 5601: Kibana

Cuando Kibana esta arrancado por primera vez, necesita una configuración del index pattern.

#### A traves  de la interfaz gráfica de Kibana

**NOTA**: Necesitamos injectar los datos de logstash antes de configurar el index pattern. Despuesde lo que hay que hacer es pulsar el button *Create*.

Para mas información sobre como se configura el index pattern puede visitar la documentación official a traves de este enlace [conectar Kibana con Elasticsearch](https://www.elastic.co/guide/en/kibana/current/connect-to-elasticsearch.html) .
