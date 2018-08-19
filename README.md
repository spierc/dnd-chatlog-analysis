# Chatlog Analysis of my friends and I's online Dungeons and Dragons game

On (most) Sunday nights, my friends and I get together to play Dungeons and Dragons (D&D) in an online chatroom called Roll20. 
Because D&D uses dice as a main mechanic for playing, Roll20 has a "dice roller" feature. However, one particular friend of mine 
insists that he is allows shafted with poor rolls (ie, rolls near or on the number 1, out of 20), and so this is an attempt 
to see if Roll20 really does hate my friend or not.

This is for you Dave.

#### Alterations to the data (done for easier parsing):

grep -o "http.*" IXChats_orig.txt > IXChats_weblinks.txt 

grep -v "http.*" IXChats_orig.txt > IXChats_nolinks.txt

sed '/Roll:/!s/: /:\n/g' IXChats_nolinks.txt > IXChats_final.txt #add a newline to places after the ":", except for if it is "Roll:"

