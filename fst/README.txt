  599  ls ../fst/
  600  xfst -e "load ../fst/brlex02.fst" -e "write prolog > brlex02.pl" -q
  601  aqua brlex02.pl 
  602  xfst -e "load ../fst/tokenizer.fst" -e "write prolog > tokenizer.pl" -q
  603  xfst -e "read prolog tokenizer.fst" -e "save stack tokenizer.fst" -e
  604  xfst -e "read prolog tokenizer.pl" -e "save stack tokenizer.fst" -q
  605  xfst -e "read prolog brlex02.pl" -e "save stack brlex02.fst" -q
  606  xfst -e "read prolog brlex02.pl" -e "save stack brlex02.fst" -stop
  607  xfst -e "read prolog tokenizer.pl" -e "save stack tokenizer.fst" -stop
  608  history | tail >> fst/README.txt
