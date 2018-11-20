### RUN frp

vim frpc.ini

docker run --name frpc -v /opt/frpc/conf:/opt/conf -d --privileged jianwenz/frpc:0.21


### RUN openvpn

vim client.ovpn

docker run --name openvpn -v /opt/ovpn-data/:/etc/openvpn -d -p 1194:1194 --privileged jianwenz/openvpn
