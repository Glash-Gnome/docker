FROM nginxinc/nginx-unprivileged:1.21-alpine

COPY ./nginx.conf /etc/nginx/nginx.conf
#COPY ./entrypoint.sh /entrypoint.sh

#RUN chown -R nginx:nginx /usr/share/nginx/html && chmod -R 755 /usr/share/nginx/html && \
#        chown -R nginx:nginx /var/cache/nginx && \
#        chown -R nginx:nginx /var/log/nginx && \
#        chown -R nginx:nginx /etc/nginx \
        # ---
#        touch /var/run/nginx.pid && \
#        chown -R nginx:nginx /var/run/nginx.pid

#ENTRYPOINT ["/entrypoint.sh"]
