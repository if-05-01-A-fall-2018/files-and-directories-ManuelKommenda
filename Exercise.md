### 1. FAT Main Memory Requirements

1) 262 144 000‬
2) same as Blocks
3) int(32 bit) Physical Block and int(32 bit) next Block
4) 262 144 000 * 64 / 8 = 2,097152 GB

### 2. Random Access of Files

a)  107834590 / 1024 = 105 307,217
    10 + 256 + 265^2 + 256^154
    triple direct point 1 -> double direct pointer 154 -> 81 block the 217 byte

b)You need need to finde the first block of the file and go to the 105307 block in that the position is the 217 byte


### 3. UFS (i-node) File Size
32 Bit -> 4 Byte
4 096 Byte / 4 = 1024  einträge möglich
10 * 4096 = 40960 Byte nur mit den ersten 10 eintägen möglich
1024 * 4096 = 4194 304 Bytes mit single direct pointer belegbar
1024 * 1024 * 4096 = 4294 967 296 Bytes mit double direct pointer belegbar
1024 * 1024 * 1024 * 4 096 = 4 398 046 511 104 Bytes mit triple direct pointer belegbar

### 4. UFS File Size

a)
32 bit pointer

512 / 4 = 128
128 * 512 = 65 536
128 * 128 * 512 = 8 388 608 genug für 5GB Files

1024 / 4 = 256
256 * 1024 = 262 144
256 * 256 * 1024 = 67 108 864

512 byte ist besser das sich 5GB files in einem double-indirect ausgeht, aber man bei 1024 byte auch einen double-indirect

b)
Da sich mit einer filesize mit 12GB mit 512 byte nur in einem triple-indirect ausgeht und in mit 1024 byte schon in einem double-indirect. Sind 1024 byte block besser
