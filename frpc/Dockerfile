FROM alpine:latest
ADD ./frpc /opt/frpc
ADD ./conf /opt/conf
VOLUME  ["/opt/conf"]
CMD /opt/frpc -c /opt/conf/frpc.ini
