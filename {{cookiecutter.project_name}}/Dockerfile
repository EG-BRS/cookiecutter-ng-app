FROM nginx

ENV PROFILE="test"
COPY nginx.conf /etc/nginx/conf.d/default.conf.templ
COPY dist /usr/share/nginx/html

CMD envsubst '${PROFILE}' < /etc/nginx/conf.d/default.conf.templ > /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'