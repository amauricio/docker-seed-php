FROM openresty/openresty:trusty

##create filter folder
RUN mkdir /filters

##dependencies
RUN /usr/local/openresty/luajit/bin/luarocks install luasocket

##delete default nginx conf
RUN rm -rf /usr/local/openresty/nginx/conf/nginx.conf
WORKDIR /filters

ADD nginx.conf /usr/local/openresty/nginx/conf/
ADD middleware.lua /filters
