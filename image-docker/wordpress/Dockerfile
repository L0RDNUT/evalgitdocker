# Utiliser l'image PHP avec Apache comme base
FROM php:7.4-apache

# Installer les dépendances nécessaires pour WordPress
RUN apt-get update && \
    apt-get install -y \
    wget \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# Télécharger et extraire WordPress dans le répertoire /var/www/html
RUN wget -qO- https://wordpress.org/latest.tar.gz | tar xvz -C /var/www/html --strip-components=1

# Activer le module rewrite pour Apache
RUN a2enmod rewrite

# Exposer le port 80
EXPOSE 80

# Commande par défaut pour démarrer Apache
CMD ["apache2-foreground"]
