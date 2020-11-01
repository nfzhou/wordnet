# wordnet

This is a port of WordNet (https://wordnet.princeton.edu/) to Picat. Most of the Prolog files can be compiled with Picat without change, except for "wn_s.pi" and "wn_g.pi". The original "wn_s.pl" file contains three facts that miss arguments, and make the predicate s/6 discontiguous. The missing arguments are back in "wn_s.pi". The original "wn_g.pl" file contains atoms that exceed the length limit (255). The atoms are changed to strings in "wn_g.pi". 

The default setting of Picat fails to compile "wn_g.pi" due to stack overflow. I used the folloinwg setting with a large amount of space for the stack:

picat -s 99999999
