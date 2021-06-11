FROM quay.io/azavea/django:3.2-python3.9-slim

RUN mkdir -p /usr/local/src
WORKDIR /usr/local/src
## Uncomment to install additional Python packages
# COPY requirements.txt /usr/local/src/
RUN set -ex \
&& buildDeps=" \
build-essential \
" \
&& deps=" \
postgresql-client-12 \
" \
&& apt-get update && apt-get install -y $buildDeps $deps --no-install-recommends \
## Uncomment to install additional Python packages
# && pip install --no-cache-dir -r requirements.txt \
&& apt-get purge -y --auto-remove $buildDeps
