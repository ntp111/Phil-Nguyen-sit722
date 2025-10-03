FROM nginx:alpine

# Copy nginx config first
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy static site
WORKDIR /usr/share/nginx/html
COPY . .

# If nginx.conf is in this folder, remove the duplicate from html
RUN rm -f /usr/share/nginx/html/nginx.conf || true

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
