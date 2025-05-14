flowchart TD
    A --> B(Résolveur DNS Récursif (Recursive DNS Resolver))
    B -- Requête pour l'adresse IP --> C(Serveur Racine (Root Nameserver))
    C -- Référence au Serveur TLD --> B
    B -- Requête pour l'adresse IP --> D(Serveur TLD (TLD Nameserver))
    D -- Référence au Serveur Autoritatif --> B
    B -- Requête pour l'adresse IP --> E(Serveur Autoritatif (Authoritative Nameserver))
    E -- Réponse avec l'adresse IP --> B
    B -- Réponse avec l'adresse IP --> A