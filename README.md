### RUN frp

vim frpc.ini

docker run --name frpc -v /opt/frpc/conf:/opt/conf -d --privileged jianwenz/frpc:0.21


### RUN openvpn

vim client.ovpn

docker run --name openvpn -v /opt/ovpn-data/:/etc/openvpn -d -p 1194:1194 --privileged jianwenz/openvpn


### openvpn证书

docker run -v /opt/ovpn-data/:/etc/openvpn --rm -it jianwenz/openvpn easyrsa build-client-full CLIENT nopass

docker run -v /opt/ovpn-data/:/etc/openvpn --rm jianwenz/openvpn ovpn_getclient CLIENT > CLIENT.ovpn
