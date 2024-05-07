ARG RASA_SDK_VERSION
ARG TIMEZONE
FROM rasa/rasa-sdk:${RASA_SDK_VERSION}

USER root
RUN apt update && apt install -y tzdata

COPY ./actions/ /app/actions

ENV TZ=${TIMEZONE}

RUN chgrp -R 0 /app && chmod -R g=u /app && chmod o+wr /app
USER 1001