Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

# Conversion de VCCV à ARPAsing
La liste d'enregistrement anglaise VCCV de PaintedCZ est très populaire dans la communauté d'outre-mer comme en témoigne les nombreuses librairies vocales et UST dans ce format.
Ces librairies et UST peuvent être convertie en ARPAsing standard.

## Convertir les librairies vocales
La structure des libraires VCCV sépare les enregistrements dans de nombreux sous-dossiers nommé "CC-", "CV_CVC" et ainsi de suite.
Les enregistrements doivent-être enlevé de leurs sous-dossiers et placé dans le dossier principal.
Téléchargez le fichier index [ici]() et renommez le en "index.csv" puis ajouté-le au dossier. 

Vous pouvez maintenant glisser déposer le dossier dans moresampler.exe pour que ce dernier génère un OTO ARPAsing. Cependant, **ne renommez pas les doublons**.
Il y aura des centaines de doublons, ce qui risque de mal faire fonctionner l'Assistant ARPAsing.
Télécharger [cet outil]() pour supprimer les doublons de l'OTO généré. Le maximum recommandé est entre 10 et 20.

## Converting USTs
Téléchargez [ce plugin](), décompresser-le et placer-le dans le dossier Plugin d'UTAU.
Si vous utilisez ce plugin sur une UST, tous les phonèmes CZ serons converties en arpabet.
Cependant, l'UST auras besoin d'ajustement. (Par exemple, il se peut que certaines notes aient plus que deux phonèmes.)
Ajustez l'UST à la librairie vocale utilisez.

Plugin original par ChieP
Converteur inspiré par Ivory [@TheIvoryShield]()
Plugin modifié par KLAD

---

# VCCV to ARPAsing Conversion

PaintedCZ's VCCV English reclist is popular in the overseas UTAU community, with an abundance of voicebanks and USTs available in that format. These voicebanks and USTs can also be converted to the ARPAsing standard.

## Converting voicebanks

The original organizational structure of VCCV voicebanks splits samples among several subfolders named "CC-", "CV_CVC", and so on. The audio samples should first be taken out of the subfolders and put into the main voicebank folder. Download the index file [here]() and rename it to "index.csv", then add it to the folder.  
You can now drag and drop the folder into Moresampler for OTO generation. However, **do not rename/number duplicates**. There will be hundreds of duplicates, which will cause ARPAsing Assistant to not function properly. Download {this tool} to delete the duplicates from the generated OTO. The recommended maximum is between 10-20.

## Converting USTs

Download [this plugin](), unzip, and place it in the plugins folder where UTAU is installed. Using this plugin on a UST will convert it from CZ phonemes to arpabet phonemes. However, this will not render it perfectly compatible with an arpasing voicebank immediately. (For example, some notes might have more than 2 phonemes.) Please make adjustments to fit the bank.  
Original plugin by ChieP  
Converter inspired by Ivory @TheIvoryShield  
Plugin modifications by KLAD
