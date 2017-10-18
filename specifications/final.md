# Cahier des charges Altern-intra


----
## Le projet
L’altern-intra est un projet collaboratif lancé par des étudiants visant à réduire la dette technique des outils que les étudiants doivent utiliser au quotidien de leur cursus à EPITECH.
L’objectif est d’avoir un projet auquel tout étudiant puisse participer. Il y a donc une volonté de rendre le projet accessible à tous, aussi bien au niveau technique qu’au niveau des utilisateurs.

---
## Objectifs
L'altern-intra a plusieurs objectifs visés, en terme d'utilisabilité et de pédagogie.

- __Utilisabilité:__ l'altern-intra doit proposer des fonctionnalités demandées par les étudiants, et non proposées par l'intranet actuel, ainsi que les fonctionnalités déjà présentes. L'objectif n'étant pas de refaire uniquement l'interface de l'intranet, il est important de viser des fonctionnalités que les étudiants jugent utiles

- __Pédagogie:__ l'altern-intra doit respecter certaines conditions afin d'être accepté par EPITECH en tant que projet du HUB Innovation Cloud. Le projet doit permettre aux élèves contributeurs de monter en compétences sur des technologies propres aux monde du Cloud telles que la scalabilité ou l'architecture en microservices. La stack MEAN (MongoDB, ExpressJS, AngularJS, NodeJS) a donc été choisie de par sa modernité, sa forte demande sur le marché du travail et sa popularité parmi les développeurs, dont les étudiants d'EPITECH

----
## Les fonctionnalités attendues
- __Mon compte__
    - __Création de compte / Connexion avec Office 365__:
les élèves possèdent maintenant tous un compte Office 365 fourni par l'école censé leur fournir tous les outils bureautiques dont ils ont besoin au long de leur cursus
    - Log time (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Notes (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Modules en cours (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
- __Mon planning__
    - __Timeline:__ L'agenda doit posséder une option pour afficher les informations dans une vue Gantt-like. Des exemples de ces implémentations pour le calendrier d'EPITECH peuvent être trouvés sur [Eygle](http://eygle.fr/epitech/tek3) ou sur [Roslyn](https://roslyn.epi.codes/2022/timeline/)
    - __Synchro planning avec Google / Office Agenda:__ L'utilisateur doir pouvoir, après avoir connecté son compte Google ou Office Agenda, demander à sychroniser les activités auxquelles il est inscrit sur le service d'agenda qu'il a sélectionné
    - Gestion des activités => inscription/désinscription (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
- __Mon dashboard__
    - Modules (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Activités (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Projets (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Possibilité de s’inscrire/désinscrire + token (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Personnalisation (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - __Tri des activités/modules:__ L'utilisateur doit pouvoir trier ses activités/modules en fonction des dates de fin/début, ou de l'avancement
- __Mes modules__
    - s’inscrire/désinscrire (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Voir d’un coup d’oeil les inscrits, le nb de crédits, description du module, ....: (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
- __Mes projets__
    - s’inscrire/désinscrire (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - Voir d’un coup d’oeil les inscrits, le nb de crédits, description du projet, .... (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
    - __Sujet en CDN:__ Un des problèmes récurrent au sein d'EPITECH lors des piscines et la non disponibilité des sujets lors des pics d'affluence sur l'intranet. Un stockage des fichiers sur CDN permettrait aux élèves d'accéder à leur sujets sans dépendre du reste de l'infrastructure
    - __Versioning des sujets:__ Un problème récurrent lors de la réalisation des projets est le changement inopiné des sujets. Les élèves ne se rendent souvent pas compte immédiatement que leurs sujets ont changés, ou en quoi ils ont changés
    - Recevoir des notifs lors du changement du sujet
    - __Gestion blih (CRUD):__ Il faudrait que les élèves soient capables de voir si le rendu de leur projet est valide (droits, nom du repo/binaire, ...). Toutefois pour des raisons évidentes de sécurité, nous ne souhaitons stocker ni les clés SSH des utilisateurs, ni leurs mots de passe Unix. Il faudrait dont leur demander leur mot de passe Unix lors du requétage de Bih, sans le stocker après-coup
- __Mes activités__
     - (Aucune fonctionnalité en plus de celles présentes actuellement n'ont été prévues pour l'instant)
- __E-Learning__
    - __Documents en CDN:__ mêmes problèmes que pour les sujets des projets
