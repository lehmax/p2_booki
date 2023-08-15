# Note de synthèse – Nouveau site Booki

Voici l’ensemble des points fonctionnels et techniques à prendre en compte pour le développement du nouveau site Booki.
L’ensemble de ces éléments a été validé par l’équipe Produit, il est donc important de les respecter.

## Maquettes

[Figma](https://www.figma.com/file/r9YJyUkpVdrxzBBKGH7reY/Maquettes-Booki-(desktop%2C-mobile%2C-tablette)?node-id=3%3A0&t=aSSTnHDTI9f1lLka-0)

## Spécifications fonctionnelles

|Fonction|Description|
|:-------|:----------|
|Fonction recherche | <ul><li>Les usagers pourront rechercher des hébergements dans la ville de leur choix.</li><li>Le champ de recherche est un champ de saisie, le texte doit donc pouvoir être édité par l’utilisateur.</li><li>Il faut englober ce champ dans un formulaire. La partie Recherche ne doit pas être fonctionnelle - <i>il s’agit d’une première version pour valider l’interface.</i></li></ul>|
|Liens “Hébergements” et “Activités” | <ul><li>Les textes “Hébergements” et “Activités”, situés dans l’en-tête, sont des liens. Ils doivent mener respectivement vers la section “Hébergements à Marseille” et “Activités à Marseille”.</li></ul> |
|Cartes “Hébergements” et “Activités” | <ul><li>Chaque carte d’hébergement ou d’activité devra être cliquable dans son intégralité (pas uniquement le titre).</li><li>Pour l’instant, les liens sont vides. On peut utiliser un attribut `href=”#”` pour simuler la présence d’un lien.</li></ul>|
|Cartes “Hébergements” et “Activités” | <ul><li>Les hébergements peuvent être filtrés par thématique, comme le budget ou l’ambiance</li><li>Les filtres doivent changer de couleur au survol de la souris.</li><li>Les filtres ne doivent pas être fonctionnels - il s’agit juste d’une première version pour valider l’interface..</li></ul>|

## Spécifications technique

|Thème |Informations techniques|
|:-----|:----------------------|
|Maquettes|Trois maquettes ont été réalisées : desktop, tablette et mobile.|
|Breakpoints|Nous avons convenu avec le designer UI d’utiliser 1024 px et 768 px :<ul><li>>1024 px pour les écrans d’ordinateurs</li><li>>=768 px pour les tablettes ;</li><li>et tout ce qui est en dessous de 768 pour les téléphones portables</li></ul>|
|Largeur min - max|Pour éviter d’étirer la page web sur la largeur de façon excessive, il va falloir déterminer une largeur maximum de 1440 px. Au-delà, une marge blanche doit apparaître sur les côtés et le contenu doit se limiter à 1440 px de large. La largeur minimum est fixée à 320 px, en-deçà de cette largeur, le comportement n’est pas garanti.|
|Desktop first|Il faut d’abord réaliser l’intégration pour les ordinateurs (autrement dit, en desktop first), puis les tablettes et enfin les téléphones. L’utilisation des Media Queries nous permettra de réaliser l’intégration pour les différents supports|
|Bibliothèque d’icônes|Les icônes proviennent de la bibliothèque Font Awesome|
|Couleurs|Les couleurs de la charte sont le bleu (#0065FC), le bleu clair (#DEEBFF) et le gris pour le fond (#F2F2F2).|
|Police|La police du site est Raleway. Nous pouvons passer par Google Fonts pour importer facilement cette police dans le code : https://fonts.google.com/specimen/Raleway|
|Mise en page|Il est recommandé d'utiliser Flexbox.|
|Balises sémantiques|Il est important d’utiliser des balises sémantiques, au minimum “header”, “nav”, “h1-h2-h3”, “main”, “section”, “article” et “footer”|
|Validité du code|<ul><li>Aucun IDE ou éditeur de code particulier n’est imposé pour le développement.</li><li>Le code doit être valide aux validateurs W3C HTML et CSS.</li><li>Le code HTML ne doit pas contenir de propriété CSS.</li><li>Lors du passage du desktop au mobile et à la tablette, ne pas dupliquer le code HTML (exception faite dans le formulaire avec le mot “Rechercher” et l’icône de la loupe).</li><li>Privilégier l’utilisation des classes CSS pour cibler un élément, plutôt que d’utiliser le nom de l’élément lui-même.</li><li>Ne pas dupliquer des classes CSS inutilement. Exemple : si 4 éléments sont identiques du point de vue de la mise en forme, alors utiliser une seule et même classe CSS, et non pas 4.</li></ul>|
|Compatibilité navigateurs|La maquette doit être compatible avec les dernières versions de Google Chrome et de Mozilla Firefox. Il faudra tester la page web sur ces deux navigateurs.|
|Restrictions|Aucun framework CSS (type BootStrap ou Tailwind CSS) ou préprocesseur CSS (type Sass ou Less) ne doit être utilisé. Aucun autre langage ne doit être utilisé (comme JavaScript, par exemple).|
