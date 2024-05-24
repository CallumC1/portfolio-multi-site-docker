FROM nginx:latest

# Copy nginx configuration template
COPY nginx.conf.template /etc/nginx/conf.d/yourpet.conf.template

# Replace the environment variable in the template and copy to the correct location
CMD envsubst '${NGINX_SERVER_NAME}' < /etc/nginx/conf.d/yourpet.conf.template > /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'
