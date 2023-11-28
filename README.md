# TikTok-Algorithm
**TikTok Mobile API Access Algorithm, Argus &amp; Ladon Explaination**
I won't release source code as it's not made by me, but modified !
But I will teach you hand by hand !
**CREDitS: AIMADNET** (IDK If you know who he is)

### Argus Explaination
1. Protobuff (https://protobuf-decoder.netlify.app/ Use this website to decode the hex 08 d2 a4 80 82 04 10 02 18 e6 e3 91 77 22 04 31 32 33 33 2a 13 37 32 34 30 34 34 31 35 33 33 36 30 31 34 36 35 38 36 31 32 0a 32 31 34 32 38 34 30 35 35 31 3a 06 33 32 2e 32 2e 32 42 14 76 30 35 2e 30 30 2e 30 31 2d 6f 76 2d 61 6e 64 72 6f 69 64 48 c0 84 80 50 52 08 44 00 00 00 00 00 00 00 60 98 c0 b5 d5 0c 6a 06 98 1e f2 73 82 d9 72 06 7f 27 e6 4e ff 07 7a 10 08 d6 01 10 02 28 8c 04 30 22 38 f2 be b5 d5 0c 82 01 19 41 7a 30 48 66 49 68 49 62 62 31 4b 7a 50 66 67 7a 6c 4c 76 47 55 61 44 31 88 01 98 c0 b5 d5 0c a2 01 04 6e 6f 6e 65 a8 01 f0 04 ba 01 21 0a 0b 41 53 55 53 5f 49 30 30 33 44 44 10 0a 1a 0a 67 6f 6f 67 6c 65 70 6c 61 79 20 80 80 84 82 01 c2 01 84 01 4d 44 47 6b 45 70 72 52 72 6e 55 4f 4a 7a 68 36 79 57 74 6d 77 59 4b 78 6d 62 5a 34 46 43 63 6c 56 7a 63 72 70 50 6c 65 54 30 66 63 4b 78 69 4b 45 7a 42 72 45 41 4a 31 52 52 6d 7a 4e 51 43 6d 32 65 6b 48 4a 67 48 42 79 78 71 53 74 77 37 4f 55 4b 4c 31 55 51 71 66 6c 7a 61 4e 56 72 70 54 4b 39 39 6e 6d 68 64 4c 36 44 52 71 2f 73 42 43 46 72 4c 68 72 79 30 51 5a 58 32 4b 34 49 58 4c 56 76 45 3d c8 01 0a d2 01 10 08 02 12 0c 01 71 7d 02 05 d0 96 7a 83 89 29 b8 e0 01 f0 07)
2. The protobuff result a bytes like above, then turns it into hex and pad it into the format AES BLOCK SIZE but CBC16 | ACTUAL CODE: pad(bytes.fromhex(ProtoBuf(protobuff).toBuf().hex()), block_size)
3. Then you need to have sm3Output, which requires sm3Hash, AES signKey (obtained with unidbg)
