# ROT13 (rotate letters by 13)
cat file.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

# Base64 decode
base64 -d file.txt > output.txt

# Base64 encode
base64 file.txt > encoded.txt

# Hexdump to binary (reverse)
xxd -r file.txt output.bin

# Binary to hexdump
xxd output.bin > hexdump.txt

# Gzip decompress
gunzip file.gz

# Bzip2 decompress
bunzip2 file.bz2

# Tar extract
tar -xf file.tar

# Detect file type
file filename
