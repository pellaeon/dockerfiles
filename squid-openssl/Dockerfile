FROM ubuntu/squid
RUN apt-get update && apt-get remove -y squid && apt-get install -y squid-openssl iproute2 mtr dnsutils iputils-ping curl tcpdump
COPY entrypoint.sh /usr/local/bin/entrypoint.sh
#COPY interface-alias.sh /interface-alias.sh
#RUN chmod +x /interface-alias.sh
#ENTRYPOINT ["/interface-alias.sh"]

ENTRYPOINT ["entrypoint.sh"]
CMD ["-f", "/etc/squid/squid.conf", "-NYC"]
