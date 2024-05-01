FROM mongo

COPY sample_posts.json /docker-entrypoint-initdb.d/sample_posts.json


RUN echo '#!/bin/bash' >> /docker-entrypoint-initdb.d/init-db.sh && \
    echo 'mongoimport --db wanderlust --collection posts --file /docker-entrypoint-initdb.d/sample_posts.json --jsonArray' >> /docker-entrypoint-initdb.d/init-db.sh && \
    chmod +x /docker-entrypoint-initdb.d/init-db.sh


EXPOSE 27017
