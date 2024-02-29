FROM nginx:alpine
LABEL "Project"="vprofile"
LABEL "Application"="Load_Balancer"
LABEL "Maintainer"="bhargavavhp"
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
