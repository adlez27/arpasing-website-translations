Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

# Tutoriel de création de liste d'enregistrement

l'ARPAsing n'est pas une seule liste d'enregistrement inchangeable mais plutôt une méthode pour synthétiser l'Anglais dans UTAU.
Tout comme la VCV n'est pas une seule liste mais une méthode pour synthétiser le japonais.
Le seul critère pour qu'une liste d'enregistrement soit considéré comme une liste ARPAsing est sa capacité à être compatible avec le générateur automatique d'OTO de Moresampler et avec l'Assistant ARPAsing.

Vous pouvez écrire votre liste anglaise ou votre complément de la façon qui vous plaira tant que les phonèmes inclus soient en Arpabet.
Une fois votre liste écrite, vous devrez créer un fichier index.csv pour que le générateur d'OTO de Moresampler sache comment configurer votre librairie vocale. 

Si vous écrivez un supplément à une liste déjà existante, vous devrez simplement ajouter vos nouveaux phonèmes à l'index.csv de la liste concernée.
Si vous créez une toute nouvelle liste, vous devrez faire un nouveau ficher index.
Vous pouvez utiliser n'importe quel éditeur de texte pour en créer un mais vous pourriez aussi utiliser l'éditeur de .csv de votre choix.

La première colonne de l'index contient tous les noms de fichiers ; ces noms sont généralement les mêmes que ceux de la liste d'enregistrement que vous utiliserez dans OREMO.
Vous devez inclure l'extension du fichier. Si vous utilisez un éditeur de texte, séparez cette colonne des autres colonnes avec une virgule.
La seconde colonne a la version en Arpabet des noms de fichiers de la première colonne.
Chaque phonèmes doivent être séparés avec un tiret du 8.

Tous les phonèmes Arpabet sont acceptés, à part ces derniers :

[em] [en] [eng] [el] [nx] [dx]

Ces phonèmes sont susceptibles d'être ajoutés à l'avenir.

Si vous avez implémenté de nouveaux phonèmes dans votre librairie vocale, vous devrez re-générer l'OTO de cette dernière afin que les doublons soient proprement numérotés.

Pour rendre les enregistrements plus agréables, vous pourrez aussi créer un ficher de commentaire OREMO. Ce fichier se nomme "OREMO-comment.txt" et se place directement dans le fichier de destination de votre librairie vocale.
La première colonne contient tous les noms des fichiers et ceux-ci correspondent aux noms de la liste d'enregistrement.
L'extension des fichiers n'est pas nécessaire, les noms de fichiers doivent seulement être les mêmes que ceux de la liste d'enregistrement.
Séparez les colonnes avec une tabulation. La colonne suivante possède le commentaire ; C'est ici que vous pouvez écrire vos notes afin de savoir comment l'enregistrement doit être prononcé.

---

# ARPAsing Reclist Writing Tutorial

ARPAsing is not a single, static reclist, but a method of English UTAU. It's similar to how VCV isn't a single reclist, but a method of Japanese UTAU. The only criteria for a reclist being an arpasing reclist is compatibility with Moresampler's auto-OTOer, and with the ARPAsing Assistant plugin.

You can write your English reclist or reclist addon in any way you like, as long as the phonemes you include directly correspond to Arpabet. Once it's written, you'll need to make an index.csv file in order for Moresampler to know how to OTO it.  
If you're writing a reclist addon, you can simply add to the existing index.csv for that reclist. If you're making a list from scratch, you'll have to make a new index file. You can use any text editor to create one, but you could also use any csv editor you like.

The first column contains all the file names, which is generally exactly the same as the reclist file you would use in OREMO. You need to include the file extension. If using a text editor, separate this column from the next column with a comma. The second column has the arpabet version of the phonemes for that line. Each phoneme must be separated by an underscore.  
Alternatively, you can write your reclist directly in Arpabet to begin with, and separate each phoneme with an underscore. This removes the need to write an index.csv at all.

All arpabet phonemes are accepted by Moresampler's auto OTOer, except these:  
`[em] [en] [eng] [el] [nx] [dx]`

If you've made a reclist addon, you must regenerate the OTO for the whole bank, so that duplicates can be properly numbered.

In order to make recording easier, you can also make an OREMO comment file. This file is named "OREMO-comment.txt" and goes in the destination folder of the voicebank. The first column contains all the file names, corresponding to the reclist. File extension is not necessary, it just needs to match up to the reclist file. Separate the columns with a tab. The next column has the comment, which is where you can write notes, like how the sample is meant to be pronounced.
