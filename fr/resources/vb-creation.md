Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

# Tutoriel de création de librairie vocale

Ce tutoriel parle des enregistrements et de la configuration de l'OTO.

Bien que vous soyez libre de choisir n'importe quel logiciel pour enregistrer votre voix, il sera bien plus facile d'utiliser OREMO.
Si vous n'êtes pas familier avec ce programme, voyez ce tutoriel comme une occasion d'apprendre à utiliser ce logiciel.

Téléchargement Officiel: [OSDN]()

Wine wrapper pour macOS: [UTAForum]()

Mac native+traduction anglaise: [UTAForum]()

(Si vous êtes sur mac, nous recommendons d'utiliser le wine wrapper car la version mac native ne possède pas de boite commentaire.)

Si vous ne pouvez pas utiliser OREMO, vous pouvez vous référer au PDF dans le téléchargement d'ARPAsing sur le site de Kanru Hua.
Faites défiler le PDF pour trouver le tableau de la liste d'enregistrement, renommez ensuite chaque fichiers avec son nombre correspondant.

Pour commencer, téléchargez la dernière liste d'enregistrement par défaut depuis la [page des listes d'enregistrements]().

Le dossier contient trois fichiers listes, un fichier commentaire OREMO et un fichier index.

La liste "core" va de 000 à 119, les "n gram" de 220 à 319 et les voyelles isolées de 320 à 334.

Le fichier de commentaire OREMO vous permet de voir les phonèmes ou mots qui correspondent à chaque chiffres.

Le fichier index est une référence pour quand moresampler génèrera l'OTO.

Si vous utilisez une reclist autre que la reclist par défaut, il y aura toujours les listes, l'index et le commentaire OREMO.

Créez un dossier pour votre librairie vocale et copié-collé le fichier index.csv ainsi que le fichier  OREMO-comment.txt dans votre dossier.
Dans OREMO, ouvrez la liste "core".
(Quand vous aurez finis cette liste, changer pour la liste des n gram puis celle des voyelles.)
Veillez à bien la destination des enregistrements dans le dossier de votre nouvelle librairie vocale.

Vous pouvez enregistrer avec ou sans guideBGM.
Si vous voulez utiliser une guideBGM, nous recommandons d'utiliser une faite pour les listes CVVC.
La CVVChinese BGM ou la VCCV English BGM sont de bons choix.

The comment file will tell you how to pronounce it approximately using words, and precisely using arpabet phonemes.
[Cet article]() va vous expliquer comment lire et prononcé l'arpabet.

À pars les suites de voyelles, chaque suites de phonème possède un type de voyelle.
Les trois syllabes rimerons.

Chantez les trois syllabes consécutivement, comme si vous enregistrez en VCV.
S'il y a un "q" dans la phonétique (ou une apostrophe dans le mot) cela veut dire que vous devez faire une courte pause.
Pour vous aider, vous pouvez télécharger une librairie vocal depuis le  [répertoire des librairies vocales]().

**POUR LES MULTIPITCH: **Pour les librairies vocales multipitch:
Il doit y avoir un pitch avec un OTO sans suffixes dans le dossier principal de votre librairie.
Tous les autres pitch avec suffixes doivent être dans leur propre sous-dossier.
N'ajoutez pas de suffix au nom des fichiers, l'index.csv serait incompatible.

Penchons-nous sur l'OTO ! Pour que moresampler effectue la configuration de la librairie vocale, glisser déposer votre dossier sur moresampler.exe.

Une fois la fenêtre ouverte, appuyez sur trois pour sélectionner ARPAsing.
Répondez "y" ou "yes" lorsque le programme vous demande qi il doit renommer les doublons.
Vous pourrez aussi choisir d'inclure un suffixe dans votre OTO.
Sachez cependant qu'il n'est pas possible d'utiliser des kanjis ou des signes tels que des flèches.

Si vous êtes sur Mac ou Linux, devrez utiliser wine pour executer Moresampler.
Ouvrez le terminal dans le dossier ou moresampler.exe se situe et écrivez "wine moresampler.exe /path/to/voicebank".
Si vous ne pouvez pas effectuer cette action, transféré vos fichiers sur un ordinateur window ou demander à un ami avec un ordinateur window de générer les fichiers.

Maintenant que votre OTO de base est généré, il faut l'ajuster.
Chaque entrées de l'OTO est un diphone, il y a que deux phonèmes ou deux sons.
En général, le premier son connecte la note à la précédente alors que le deuxième son est la note en elle-même.
Pour configurer votre OTO, trouvez tout d'abord la section qui correspond au premier phonème puis la section qui correspond au second phonème.

## Premier phonème

**[-]**

La quantité d'overlap n'a pas d'importance pour celui-ci car ces notes viennent toujours au début d'une phrase, après un rest.
La seule chose importante est qu'il doit y avoir une zone de silence.

**[c]**

_Consonnes non voisée (p t k)_

Si ceci est le premier phonème de l'enregistrement, déplacez l'offset de façon à ce que l'overlap soit à 15msec de la consonne.
S'il y a d'autres phonèmes avant celui-ci, déplacez l'offset là où le précédent se terminait.
Assurez-vous de ne pas entendre le précédent. Placez l'overlap à 15msec de la consonne.

_Consonnes voisées et fricatives (b d g ch jh)_

Si ceci est le premier phonème de l'enregistrement, déplacez l'offset de façon à ce que l'overlap soit là où la consonne commence.
S'il y a d'autre phonème avant celui-ci, déplacez l'offset là où le précédent se terminait.
Assurez-vous de ne pas entendre le précédent. Déplacez l'overlap là où la consonne commence.

_Fricatives, nasales et liquides (f v th dh s z sh zh hh m n ng l r)_

Déplacez l'offset là où la consonne commence.
Vous devriez avoir recours à la section sur les semi-voyelles pour le "r" en particulier.

_Semi-voyelles (y w)_

Ces consonnes peuvent être difficile à voir sur une sonore.
En appuyant sur le bouton [s], vous pouvez enclencher le spectrogramme.
Les zones les plus claires sont les fréquences les plus fortes.
Les semi-voyelles se caractérisent par un changement de fréquence.
Déplacer l'offset là où la consonne commence puis placer l'overlap là où la fréquence est consistante avant le changement.
La pre-utterance va se placer après le changement.

**[v]**

La quantité d'overlap pour ces enregistrements doit être suffisamment haute par défaut.
Si elle est basse, la déplacer de 50msec doit faire l'affaire.

Déplacez l'offset initial pour que la zone entre ce dernier et l'overlap soit à un niveau consistent.

## Second Phonème

Dans tous les cas, la pre-utterance doit être placée là où le premier phonème se termine et ou le second phonème commence.

**[c]**

_Stops (p b t d k g ch jh)_

Il devrait avoir un morceau de silence juste avant la consonne.
Déplacez le rose là où le silence commence et déplacez le cutoff là où le silence se termine.
La consonne en elle-même n'est pas incluse car dans une UST, cette note est suivie d'une autre notre qui possède une consonne.

_Fricatives (f v th dh s z sh zh hh)_

Couvrez toute la consonne avec du rose et arrêtez-vous avant la fin de la consonne.
Déplacez le cutoff au même endroit en laissant un petit espace entre les deux.
Sans cet espace, les resamplers ne pourront pas synthétiser l'enregistrement.

Si il y a du silence après la consonne, laisser la zone blanche en tant que silence.

_Nasales, liquides et semi-voyelles (m n ng l r y w)_

Déplacez la zone rose là où la consonne commence à être stable et consistante.
Utilisez le cutoff pour couper l'effacement de la consonne.
Ces consonnes peuvent être étirées.

**[v]**

Déplacez la zone rose là où la voyelle commence à être stable et consistante.
Utilisez le cutoff pour enlever l'effacement de la voyelle.

**[-]**

Couvrez tout avec du rose.
La zone blanche doit être composée que de silence.

Votre librairie vocale est déjà terminé.
Si vous avez besoin de dessins pour votre librairie, Partial en offre gratuitement sur [ce sujet]().
Veuillez soumettre vos librairies complètes dans le répertoire adapté.
Amusez-vous bien et bonne chance !

---

# Voicebank Creation Tutorial

This tutorial covers both recording and OTOing.

While you can use whatever you like to record, it will be much, much easier to use OREMO. If you're currently unfamiliar with how to use it, see this as an opportunity to learn how. If you plan to do sample processing, you'll have to do it after recording.  
Official download: [OSDN]()  
Wine wrapper for macOS: [UTAForum]()  
Mac native English translation: [UTAForum]()  
(I recommend the wine wrapper, because the mac native version doesn't have the comment box.)

To begin, download the latest default reclist from [the reclist page](). You can choose either the version with or without the index. If not using OREMO, the version without the index will be much easier to read.

If you are using the list with the index:
- The folder contains a reclist file, OREMO comment file, and index file.
- The reclist is numbers 000 to 334.
- The OREMO comment file allows you to see the actual phonemes or words that correspond with each number.
- The index file is for moresampler to reference when generating the OTO.

If you are using the list without the index:
- The folder contains a reclist file and OREMO comment file.
- The reclist contains arpabet phonemes.
- The OREMO comment file allows you to see the words that correspond with the phonemes.
- No index file is necessary, because moresampler can read the file names as-is.

Set up a folder for your voicebank, and copy+paste OREMO-comment.txt (and index.csv if applicable) into your new folder. In OREMO, open the reclist. Set the destination folder to your new folder.

You can record with or without guideBGM. If you want to use guideBGM, I recommend using a short one made for CVVC reclists, such as the CVVChinese BGMs or the VCCV English BGMs.

Note to translator: These next two lines were written for english speakers.

The comment file will tell you how to pronounce it approximately using words, and precisely using arpabet phonemes. [This short article]() will explain how to read and pronounce arpabet. It's actually pretty straightforward! If you're already familiar with another phonetic system like PaintedCZ's system or X-SAMPA, refer to the chart on [this page]().
Other than vowel strings, each string only has 1 type of vowel. All three syllables will rhyme.

Note to translator: Please write a new section here about how to properly pronounce English phonemes, for people who may be unfamiliar with them.

Sing the 3 syllables consecutively, as if recording VCV. If at any point there is a "q" in the phonetics (or an apostrophe in the words) it means a brief pause (a glottal stop).
For reference, you can download existing voicebanks from the [voicebank directory]().

**FOR MULTIPITCH:** The main voicebank folder must contain a pitch that does not have any suffixes. All other pitches must be placed in subfolders. When recording, do not add suffixes to the file names, or Moresampler won't be able to read the index.csv while OTOing.  
**FOR EXTRA SAMPLES:** Any extra samples that aren't standard in ARPAsing must be placed in a subfolder, so that they will have a separate oto.ini file. This enables ARPAsing Assistant to properly read the main oto.ini file with only standard ARPAsing OTO entries.

Onto OTOing! Simply drag and drop the folder onto moresampler.exe to do so.  
Enter 3 to choose arpasing. When prompted on renaming duplicates, enter y or yes. Whenever there are multiple of the same diphone, such as [s t], this will add a numeric suffix to the end of additional copies. This serves to distinguish each one from the other, as they may sound different based on the context of nearby phonemes in the string. You can also choose whether or not to include a suffix. It's not possible to use characters such as arrows or kanji, so you will have to use suffixes such as "S" or "A#3".

If you are using Mac or Linux, you will have to use wine to run Moresampler. Open terminal in the folder that moresampler.exe is in, and type "wine moresampler.exe /path/to/voicebank". If you're unable to do this, transfer your files to a windows computer, or ask a friend with Windows for help to generate it.

Now that your base OTO is generated, it's time to refine it. Every entry of the OTO is a diphone, meaning that there are only two phonemes or two sounds. In general, the first one is a connector to the previous note, while the second one is the main phoneme for the current note. To OTO, first find the section corresponding to the first phoneme, then find the section for the second phoneme.

## First phoneme

This covers the blue offset and overlap.

**[-]**  
The amount of overlap really doesn't matter for this one, because these notes always come at the beginning of a phrase, right after a rest. The only important thing is that it covers an area of silence.

**[c]**  
*Unvoiced plosives (p t k)*  
If this is the first phoneme in the string, move the offset such that the overlap ends up about 15msec before the consonant.
If there are other phonemes before this one, move the offset to where the previous one ended. Make sure you can't hear the previous one. Place the overlap about 15msec before the consonant.

*Voiced plosives and affricates (b d g ch jh)*  
If this is the first phoneme in the string, move the offset such that the overlap ends up where the consonant begins.  
If there are other phonemes before this one, move the offset to where the previous one ended. Make sure you can't hear the previous one. Place the overlap where the consonant begins.

*Fricatives, nasals, and liquids (f v th dh s z sh zh hh m n ng l r)*  
Move the offset to where the consonant begins. For 'r' in particular, you may want to refer to the glides section for help.

*Glides (y w)*  
These consonants can be difficult to see on a normal waveform. By clicking on the [s] button, you can switch to spectrogram view, which gives you another way to visualize the audio. The bright areas are the loudest frequencies. These consonants show up as a change in frequencies over time.  
Move the offset to where the consonant begins, then place the overlap where it's consistent before the change. The preutterance will end up after the change.

**[v]**  
By default, the overlap for these samples should be at a decently high amount. If it's absurdly small, moving it to around 50msec should be good.  
Move the initial offset so that the area between it and the overlap is at a consistent level.

For diphthongs, the overlap should cover the area before the vowel changes.

## Second Phoneme

For all cases, the preutterance should be placed where the first phoneme ends and second phoneme begins. This also covers the pink area, white area, and blue cutoff.

**[c]**  
*Stops (p b t d k g ch jh)*  
There should be a small bit of silence or near silence just before the consonant. Move the pink where the silence begins, and the cutoff to where the silence ends. Yes, we're not including the consonant itself. That's because, in a UST, this note would be followed by another note that DOES have the consonant. This allows for a smooth transition without an awkward double consonant sound.

*Fricatives (f v th dh s z sh zh hh)*  
Cover the entire consonant with pink until just before the end. Bring the cutoff to the same place, leaving a tiny gap. Without this gap, resamplers won't be able to render it. However, we don't want these consonants to be stretched.

If there is silence after the consonant, have the white area be silence instead.

*Nasals, liquids and glides (m n ng l r y w)*  
Move the pink to where the consonant starts being stable and consistent. Use the cutoff to remove where the consonant ends or fades out. These consonants are safe to stretch.

**[v]**  
Move the pink to where the vowel starts being stable and consistent. Use the cutoff to remove where the vowel fades out. The white area will be the sustained part of the note, which ensures that it will sound good.

For vowel-vowel diphones, place the preutterance at the end of the vowel change.

For diphthongs, place the cutoff before the vowel changes.

**[-]**  
Cover everything with pink, such that everything in white is silence.

And just like that, your voicebank is already done. Please submit any released banks to the directory. Have fun, good luck!
