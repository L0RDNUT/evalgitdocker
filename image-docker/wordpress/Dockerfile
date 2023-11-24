# Utiliser une image PHP avec Apache
FROM php:7.4-apache

# Copier les fichiers de l'application WordPress dans le conteneur
COPY ./wordpress /var/www/html/

# Activer le module rewrite pour Apache
RUN a2enmod rewrite

# Exposer le port 80
EXPOSE 8001

# Commande par défaut pour démarrer Apache
CMD ["apache2-foreground"]
