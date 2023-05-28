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
