<p align="center">
  <a href="https://ag.tavardt.com/fr/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Testeur de SEO Mobile et Ergonomie Smartphone

[![Testeur SEO Mobile](https://img.shields.io/badge/TAVARDT-Mobile%20SEO-5b3cf5.svg)](https://tools.tavardt.com/fr/test-seo-mobile-google/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Audit de conformite mobile-first, configuration de la balise viewport, largeurs fixes, lisibilite des polices et ergonomie tactile.

***

## Vecteurs de Risque et Impact Operationnel sur l Experience Mobile

Les sites web depourvus de balise viewport conforme sont penalises lors de l indexation mobile-first de Google et perdent leur visibilite en France. Un dimensionnement inadapte provoque des defauts d affichage et impose un defilement horizontal repoussant.

Le blocage de la fonction de zoom enfreint les regles fondamentales d accessibilite web pour les utilisateurs malvoyants. Des largeurs rigides et des textes trop petits augmentent le taux de rebond et degradent les indicateurs de performance.

***

## Fonctionnalites Centrales d Audit Technique

* **Analyse de la Directive Viewport**: Examine la balise meta viewport, la largeur adaptee a l ecran, l echelle initiale et le blocage du zoom, retirant jusqu a 45 points en cas d absence.
* **Detection du Debordement Horizontal**: Identifie les proprietes CSS avec des largeurs fixes depassant 450px qui brisent l affichage sur smartphone.
* **Audit de la Lisibilite Typographique**: Releve les declarations de taille de police inferieures a 12px, appliquant jusqu a 15 points de penalite.
* **Evaluation des Cibles Tactiles**: Recense les liens, boutons et champs de saisie pour valider la densite et l ergonomie d interaction.
* **Verification de l Icone Tactile (Apple Touch Icon)**: Verifie la declaration du lien apple-touch-icon dans le bloc head, deduisant 5 points en cas d omission.
* **Score Global d Ergonomie Mobile**: Calcule une note sur 100 categorisee en SATISFACTORY, ADVISORY ou UNSATISFACTORY.
* **Emulation Mobile Fidele**: Envoie des requetes HTTP avec l entete User-Agent exact de Safari sur iPhone pour une observation realiste.

***

## Installation et Execution

Necessite Python 3.8 ou superieur sans aucune dependance externe obligatoire.

```bash
git clone https://github.com/TAVARDT-France/mobile-seo-tester-fr.git
cd mobile-seo-tester-fr
python mobile_seo_tester.py https://societe.fr
```

Pour generer la sortie au format structure JSON dans vos pipelines d integration continue:

```bash
python mobile_seo_tester.py https://societe.fr -j
```

***

## Foire Aux Questions Techniques (FAQ)

### 1. Quel est l impact d une balise viewport absente ou mal configuree pour l indexation mobile?
Les robots de recherche indexent desormais les sites exclusivement a travers le rendu sur smartphone. En l absence d une balise viewport declarant device-width, le navigateur affiche une mise en page d ordinateur et retrograde severement le positionnement.

### 2. Pourquoi l outil sanctionne-t-il le blocage du zoom par l attribut user-scalable=no?
Interdire le redimensionnement manuel constitue un obstacle majeur pour les utilisateurs necessitant un agrandissement visuel. Les moteurs de recherche assimilent ce verrouillage a un defaut d ergonomie et baissent le score global du site.

### 3. Comment les conteneurs a largeur fixe superieure a 450px nuisent-ils a l ergonomie mobile?
Les elements de mise en page rigides depassant 450px excedent la largeur d ecran des smartphones et contraignent a un defilement horizontal. Cette rupture de la continuite fluide entraine un echec systematique aux tests d adaptabilite mobile.

### 4. Quels sont les risques operationnels lies aux polices d ecriture de moins de 12px?
Les textes de moins de 12px provoquent une fatigue visuelle immediate sur les ecrans d appareils portables a forte densite de pixels. L outil deduit des points pour garantir que le texte soit lisible des le chargement sans intervention de l utilisateur.

### 5. Pourquoi est-il indispensable de declarer l icone apple-touch-icon dans le code source?
La balise apple-touch-icon permet aux systemes d exploitation mobiles d afficher une vignette de marque soignee lors de l ajout a l ecran d accueil. L omission de ce lien entraine la creation d icones ternes par defaut qui diminuent l image de marque.

***

## Conseil en SEO Mobile et Architecture Responsive

Pour les portails a fort trafic exigeant une conformite rigoureuse aux standards Google Mobile-First Indexing et W3C, faites appel a l equipe de **TAVARDT**.

***

## Liens Utiles

* **Portail Institutionnel:** https://ag.tavardt.com/fr/
* **Suite de Diagnostics:** https://tools.tavardt.com/fr/
* **Contact Technique:** https://ag.tavardt.com/fr/contact/

***

### Licence
Distribue sous licence MIT. Consultez le fichier LICENSE pour plus d informations.

***

© 2026 TAVARDT. Tous droits reserves.
