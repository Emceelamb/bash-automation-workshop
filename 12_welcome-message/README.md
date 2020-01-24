# This will display a Jenny Holzer truism each time a terminal is opened.

1. Download Truisms: `wget https://raw.githubusercontent.com/carlpeaslee/hlzr/master/truisms`
2. Format text (There a few cli ways to do this)
  - use awk to remove empty fields and output to new file: `awk 'NF' truisms > truisms`
  - Use sed to edit in place: `sed -i '/^$/d' truisms`
3. Create the randomizer script
4. Call script from `.bashrc`
