# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080


LABEL io.k8s.description="a basic apache http server child image, uses OBBUILD" \
      io.k8s.display-name="Apche HTTP servers" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, http"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chgrp -R g=u /var/log/httpd /var/run/httpd

USER 1001


