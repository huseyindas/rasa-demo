ARG RASA_VERSION
FROM rasa/rasa:${RASA_VERSION}

USER root
RUN apt update -y

COPY ./rasa/ /app/

RUN chgrp -R 0 /app && chmod -R g=u /app && chmod o+wr /app
USER 1001