# Pseudonymisation
Voici un exemple d'une façon de dépersonnaliser des données dans une feuille de calcul. Il existe de nombreuses façons de procéder à la déper-sonnalisation. Cet exemple utilise un "code clé" pour supprimer les informations personnelles identifiables contenues dans les identifiants directs et les conserver dans un fichier séparé. Les informations personnellement identifiables (PII) sont des informations qui peuvent être utilisées pour identifier un individu. Les exemples courants sont le nom, l'adresse, le numéro de téléphone, la date de naissance et le numéro de sécurité sociale ou d'identification nationale.

L'exercice utilise [un ensemble de données type qui se trouve dans le dossier de données du guide en ligne](data/Pseudonymization_example.csv). Une fois que vous avez pseudonymisé les données de l'échantillon, vous pouvez continuer avec le tutoriel  [pour effectuer une évaluation du risque de divulgation](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/).

## Étape 1 - Identifier les informations personnelles identifiables (PII)
Commencez par identifier les (PII) dans les données. Idéalement, vous disposerez de métadonnées - don-nées ou document définissant vos données - pour vous aider à comprendre quels champs contiennent des (PII). Dans les données de l'échantillon, il y a trois colonnes qui contiennent des (PII) potentielles :
- `#respondee +name` semble contenir un nom.
- `#respondee +code` contient probablement un numéro d'identification quelconque.
- `#respondee +contact` contient éventuellement un numéro de téléphone mobile.

Chacun de ces identificateurs directs utilise le [Humanitarian Exchange Language pour le balisage des données](https://hxlstandard.org).

![Find PII](images/Step1-Find-PII.png)

## Étape 2 - Créer de nouvelles colonnes pour le code clé
Nous utiliserons un code clé, une valeur que nous générons, pour extraire les (PII). Puisque les identifiants directs sont tous regroupés, nous allons créer deux nouvelles colonnes entre les colonnes C, `#respondee +contact` et la colonne D , `province`. Dans Excel, nous faisons cela en mettant en surbrillance une colonne à droite de l'endroit où nous voulons insérer de nouvelles colonnes, en faisant un clic droit sur la colonne et en sélectionnant `Insérer`. Répétez ce processus pour créer une autre colonne vide.

![Create New Columns](images/Step2-create-columns.png)

## Étape 3 - Créer le code clé
Commencez par nommer vos nouvelles colonnes. Nous utiliserons un « code clé » dans chacune d'elles : chaque colonne contiendra les mêmes valeurs. Ce serait le bon moment pour mettre à jour les métadonnées de cet ensemble de données afin d'expliquer la signification du `code clé` ! Ensuite, nous allons utiliser  [la fonction de remplissage automatique d'Excel](https://support.microsoft.com/en-us/office/fill-data-automatically-in-worksheet-cells-74e31bdd-d993-45da-aa82-35a236c5b5db) pour créer un code simple. Tapez `Respondee01` dans la première cellule. Ensuite, mettez cette cellule en surbrillance, cliquez sur la poignée de déplacement dans le coin inférieur droit de la cellule et faites-la glisser jusqu'à la fin de l'ensemble de données. Le numéro final de chaque enregis-trement sera automatiquement complété, de sorte que chaque personne interrogée aura désormais un nouveau code.

![Create Key Code](images/Step3-create-key-code.png)

## Étape 4 - Dupliquer le code clé et supprimer les formules
Nous allons maintenant copier le code clé et le coller dans la colonne adjacente. Pour ce faire, vous pouvez utiliser des commandes clavier de base telles que `ctrl + C` ou mettre en surbrillance les cellules que vous souhaitez copier, faire un clic droit dessus et sélectionner `Copier`. Dans la colonne adjacente, mettez en surbrillance les cellules dans lesquelles vous souhaitez coller le nouveau code clé, faites un clic droit et choi-sissez `Coller`. J'ai choisi de ne coller spécifiquement que les valeurs. Si vous avez utilisé une formule pour créer un nouveau code, il sera important de ne con-server *que les valeurs* pour les utiliser comme code clé !

![Duplicate Key Code](images/Step4-duplicate-key-code.png)

## Étape 5 - Séparer les identifiants directs et indirects
Mettez en évidence les colonnes qui contiennent les identificateurs directs avec les (PII) ainsi qu'une des colonnes de code clé. Dans cet exemple, nous mettons en surbrillance les colonnes A-D. Cliquez dessus avec le bouton droit de la souris et sélec-tionnez `Couper`.

![Separate the data](images/Step5-separate-data.png)

Ensuite, ouvrez une nouvelle feuille de calcul et collez ces valeurs en utilisant le raccourci clavier `ctrl + v`, ou une autre méthode. Enregistrez la nou-velle feuille de calcul. Vous avez maintenant deux feuilles de calcul : l'une d'elles contient les identifiants indirects tandis que la nouvelle feuille contient les identifiants directs avec les (PII). Les deux ensembles de données contiennent un code clé pour chaque enregistrement des données afin que toutes les données puissent être recombinées si nécessaire.

![Separate the data](images/Step5a-separate-data.png)

## Étapes suivantes
Les deux dossiers contiennent un code clé qui permettra de les reconstituer. Une façon d'y parvenir dans Excel est d'utiliser la [fonction `VLOOKUP`](https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1) pour remplir automatiquement les cellules en fonction de la valeur d'autres cellules. Dans ce cas, vous pouvez remplir les cellules vides du fichier d'origine avec les (PII) manquantes en vous basant sur la valeur du `code clé`.

Comme le nouveau fichier contient les identifiants directs contenant les (PII), il doit être stocké de manière sécurisée. Un excellent moyen d'y parvenir est de crypter le fichier et d'utiliser le stockage en nuage pour limiter les personnes ayant accès au fichier (voir les guides *Meilleures pratiques en matière de partage de fichiers* et *Cryptage d'un fichier*).   

**N'oubliez pas : si la feuille de calcul originale a été dépersonnalisée en supprimant les identifiants directs qui contiennent des (PII) évidentes, les autres identifiants indirects peuvent être combinés avec d'autres données ou analysés de manière à permettre l'identification d'une personne.** Pour cette raison, les deux fichiers doivent toujours être stockés de manière sécurisée. Si vous souhaitiez partager plus largement le fichier original, sans PPI, il serait essentiel de procéder à *une évaluation du risque de divulgation* afin de garantir le risque minimum que les données puissent être réidentifiées. Le Humanitarian Data Centre dispose d’un [tutoriel en ligne permettant de réaliser une évaluation du risque de divulgation](https://centre.humdata.org/learning-path/disclosure-risk-assessment-overview/) à l’aide du [logiciel statistique à code source ouvert « R »](https://www.r-project.org/). De plus, la page web [Poverty Action Lab's *De-identification for data publication*](https://www.povertyactionlab.org/resource/data-de-identification) fournit une excellente discussion sur la dé-identification des données et inclut un exemple de code pour le [logiciel statistique « Sata »](https://www.stata.com/). Pour le personnel de Mercy Corps, [l’ébauche de directive de T4D](https://docs.google.com/document/d/1wFI5Ltvu9abtuRDVVZnbY2rdR61N3Eel4egZ02HuvU0/edit?usp=sharing) est disponible en interne et fournit des formules Excel supplémentaires.  

Enfin, toutes ces mesures contribuent à atténuer le risque d'exposition des DPI. Elles doivent donc être mentionnées dans l'évaluation des inci-dences sur la vie privée (voir le guide *Evaluation des incidences sur la vie privée*) afin que les autres comprennent comment ces données sont protégées.
