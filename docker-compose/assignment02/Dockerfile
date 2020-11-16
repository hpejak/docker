FROM drupal:8.6

RUN apt update && apt install -y git && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

COPY nginx.conf /var/www/html/

WORKDIR /var/www/html