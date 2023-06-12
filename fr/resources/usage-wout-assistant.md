Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

## Utilisation des librairies vocales sans l'Assistant ARPAsing
Ce tutoriel va vous expliquer comment utiliser une librairie vocale ARPAsing dans UTAU sans l'aide de l'Assistant ARPAsing.

Il est dans votre intérêt d'avoir une librairie vocale avec un OTO complet avant de créer une UST avec car le timing des notes va dépendre de la valeur de la pre-utterance.

Si vous n'utilisez pas le plugin, vous n'aurez aucun problèmes d'erreurs de timing et de phonèmes incorrecte causées par l'Assistant.
Cependant, vous n'aurez pas le confort d'avoir une conversion de base.

Si votre ordinateur peut faire tourner l'Assistant ARPAsing mais que vous choisissez de ne pas l'utiliser, vous pouvez ouvrir te .exe en tant que programme indépendant vous étudier la conversion des mots anglais à l'Arpabet.
Si vous ne pouvez absolument pas faire tourner le programme, il existe [des sites internets]() qui convertissent les mots à votre place.
Ce dictionnaire n'est pas aussi robuste que celui de l'Assistant mais après que vous vous êtes familiarisé avec ce système phonétique vous pourrez être capable de transcrire tous les mots manquant vous-même.

Changez chaque notes avec la CV principale de la syllabe, en séparant chaque phonèmes avec un espace.
Par exemple, le mot « cat » est « K AE T » en arpabet, donc changez vos paroles par [k ae].
De la même façon, « steps » est « S T EH P S », donc entrer [t eh]. 

Les autres notes essentielles dont nous avons besoin sont les notes de fin de phrase.
Quand il y a un « rest » après une note, vous devrez le changer en phonème silencieux.
Si le rest est moins long qu’un quart de note, changez le complètement.
S’il est plus long, seul le premier quart de la note doit être changée.
Pour « cat » la note silencieuse serais un [t -] et pour « steps » ce serais un [s -].

Vous devrez ensuite entrer toutes les notes de transitions.
La liste ARPAsing fonctionne sur un système de diphone, donc toutes les notes possèdent deux phonèmes.

Les silences compte comme un phonème, ils sont nécessaire pour faire la transition entre une note chantée et un rest.
Nous avons déjà expliqué comment s’occuper des notes avec un rest après elles, donc nous allons maintenant voir les notes avec un rest avant elles.
Si la note commence avec une voyelle, ajoutez simplement un trait d’union.
Par exemple, « eye » [ay] devient [- ay].
Si la note commence avec une consonne ou un groupe de consonnes, il faut faire le chemin à l’envers et commencer depuis la dernière consonne avant la voyelle.
Prenons « strand » comme exemple. Créez une note avec [t r]  juste avant [r ae].
Créez une note avec [s t] avant [t r]. Enfinf, créez une note avec [- s] avant [s t].
Ceci vous permettra d’avoir une transition complète du silence au noyau de la syllabe en passant par les consonnes.

Pour les transitions entre les syllabes, utilisez le même principe pour transition complète de diphones en diphones.

« stranded on this island » 

[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]

La longueur des notes de transition dépendes de la pre-utterance de la note qui la suit.
Cependant, vous pouvez utiliser votre jugement personnel pour ajuster la longueur des notes.

Si une note en particulier sonne étrange ou fausse, vous pouvez utiliser un doublon de ce diphone en ajoutant un suffixe numéroté.
Exemple : de [f ey] à [f ey1] zt ainsi de suite. 

D’ici, vous pouvez tuner comme à votre habitude.

---

# Voicebank Usage Tutorial without ARPAsing Assisstant
This tutorial will explain how to use an ARPAsing voicebank in UTAU, without ARPAsing Assistant.

It is in your best interest to have a fully OTO'd voicebank, before making USTs with it, because adjusting the timing of notes will depend on preutterance values.

If you aren't using the plugin, you can bypass all of the problems involved in adjusting the timing and incorrect phonemes. However, you miss out on all the convenience of having base conversions.  
If your computer is able to use ARPAsing Assistant but you choose not to use it, you can open the exe as a standalone program to look up word-to-arpabet conversions. However, if you're completely unable to use it (for example, Mac users) you can use [this website]() to find conversions. The dictionary may not be as robust as the one built into the plugin, but after familiarizing yourself with the phonetic system you should be able to transcribe any missing words yourself. If you're not familiar with Arpabet, you can reference [this article]() or the [phoneme chart]().

Enter the plain english lyrics into the UST as you normally would, for reference.  
Change each note to the main CV of the syllable, separating each phoneme with a space. For example, the word "cat" is "K AE T" in arpabet, so change the lyric to say `[k ae]`. Likewise, "steps" is "S T EH P S", so put `[t eh]`.  
The other essential notes we need are phrase-final notes. Wherever there is a rest after a note, you need to have phoneme to silence. As a rule of thumb, if the rest is less than 1 quarter note long, change the whole rest. If the rest is longer, then only the first quarter note needs to be changed. For "cat" that would be a `[t -]` note, and for "steps" it would be `[s -]`.

The rest of it is entering transitional notes. This list works on diphones, so every lyric note has two phonemes.  
Silence counts as one, and is necessary whenever transitioning between sung lyrics and rests. We already covered notes with rests AFTER them, so let's consider notes with rests before. If it starts with a vowel, you can simply add a hyphen. For example, "eye" `[ay]` becomes `[- ay]`. If it starts with a consonant or consonant cluster, you want to work backwards from the innermost consonant. Take "strand" for example. Make a note just before `[r ae]` that has `[t r]`. Make a note just before `[t r]` that has `[s t]`. Make a note just before `[s t]` that has `[- s]`. This gets you a full transition from silence, through the consonants, to the nucleus of the syllable.  
For transitions between syllables, use this same principle of full transitions from diphone to diphone.

"stranded on this island"
`[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]`

The length of the transitional notes depends on the preutterance of the note that follows it. However, you can use your personal judgement to make them longer or shorter.  
If any particular note sounds strange or off, you can switch to using an alternate recording of the same diphone by adding a numerical suffix, like changing `[f ey]` to `[f ey1]` and so on.

From here, you can tune as normal.
