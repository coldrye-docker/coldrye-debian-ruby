FROM coldrye/debian-tini:0-9-0-jessie-latest

RUN set -ex \
    && export APT_LISTCHANGES_FRONTEND=none \
    && apt-get update \
    && apt-get -q -y -o Dpkg::Options::="--force-confdef" -o Dpkg::Options::="--force-confold" -t jessie-backports install ruby ruby-dev build-essential \
    && apt-get clean \
    && rm -Rf /var/lib/apt/lists/* 2>/dev/null

CMD [ "irb" ]
