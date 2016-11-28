FROM kibana:5.0.0

RUN apt-get update && apt-get install -y netcat

RUN kibana-plugin install x-pack

COPY entrypoint.sh /tmp/entrypoint.sh
RUN chmod +x /tmp/entrypoint.sh

CMD ["/tmp/entrypoint.sh"]