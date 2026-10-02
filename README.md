# Cloud Computing & Virtualization Labs

Ce dépôt rassemble mes travaux pratiques (TP) réalisés dans le cadre de ma formation en **L3 Informatique** à l'UAM, sous la direction du Pr. Dr Lamine YADE. Il valide mes compétences pratiques en administration système Linux, gestion des infrastructures virtuelles et conteneurisation.

---

## 📁 Structure du Projet

* **`TP2-TP3_Virtualization_Network/`** : Administration du stockage persistant et sécurisation réseau.
* **`TP4-TP5-TP6_Docker_Containers/`** : Conteneurisation, gestion du cycle de vie des applications et isolation réseau.

---

## 🛠️ Compétences Techniques Validées

### 1. Virtualisation & Administration Réseau (TP2 & TP3)
* **Gestion du stockage Linux :** Partitionnement de disques avec `parted`, initialisation de tables GPT, formatage en `ext4` avec attribution de labels de volume stables.
* **Persistance système :** Configuration avancée du fichier `/etc/fstab` à l'aide des identifiants uniques UUID et de l'option `nofail` pour pérenniser le montage au boot.
* **Réseaux isolés :** Déploiement d'une architecture réseau double sous VirtualBox (NAT avec redirection de ports pour l'administration et Host-Only pour les flux privés hermétiques).
* **Sécurisation des accès distants :** Installation et durcissement du démon `sshd` (OpenSSH Server) sur le port standard TCP/22, filtrage et validation via l'outil `ss`.

### 2. Conteneurisation & Architecture Micro-services (TP4, TP5 & TP6)
* **Cycle de vie des conteneurs :** Industrialisation d'applications web (Nginx Alpine) via Docker Engine, isolation des flux, gestion des statuts de fonctionnement (`Up`, `Exited`) et traçabilité des journaux système (`journalctl`).
* **Industrialisation par le code :** Rédaction de scripts de construction `Dockerfile` documentés et optimisés (utilisation de `.dockerignore` pour le contrôle de contexte, intégration de sondes de santé automatisées `HEALTHCHECK`).
* **Immuabilité des couches :** Validation des mécanismes de cache de build Docker et génération d'empreintes cryptographiques uniques (SHA-256).
* **Persistance & DNS embarqué :** Création de réseaux d'isolation de type *bridge* utilisateur (`campus-net`) permettant la résolution de noms entre conteneurs pairs, couplée à des volumes nommés autonomes pour décorréler les données du cycle de vie des instances.
