FROM nginx:stable

#Make Directory - Workspace
RUN mkdir -p /var/www/

#give permissions to webuser
RUN chown -R 33:33 /var/www/

COPY --chown=33:33 . .