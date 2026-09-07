# TAR archive
tar -xf file.tar        # extract
tar -tf file.tar        # list contents
tar -cf archive.tar dir # create tar from dir

# Gzip (.gz)
gunzip file.gz          # decompress
gzip file               # compress
tar -xzf file.tar.gz    # extract tar.gz in one step

# Bzip2 (.bz2)
bunzip2 file.bz2        # decompress
bzip2 file              # compress
tar -xjf file.tar.bz2   # extract tar.bz2 in one step

# XZ (.xz)
unxz file.xz            # decompress
xz file                 # compress
tar -xJf file.tar.xz    # extract tar.xz in one step

# General tip: always check file type
file filename           # detect compression type

