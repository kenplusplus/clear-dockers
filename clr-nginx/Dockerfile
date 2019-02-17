FROM clearlinux
MAINTAINER ken.lu@intel.com

ARG swupd_args

RUN swupd update $swupd_args
RUN swupd bundle-add nginx

RUN rm -rf /var/lib/swupd

# forward request and error logs to docker log collector
#RUN ln -sf /dev/stdout /var/log/nginx/access.log \
#	&& ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80

STOPSIGNAL SIGTERM

CMD ["nginx", "-g", "daemon off;"]
