# Challenge Description

https://www.hust.edu.vn/vi/news/hoat-dong-chung/tri-tue-bach-khoa-tung-buoc-hien-dien-tren-ban-do-an-toan-thong-tin-the-gioi-655002.html

**Attachment:** [chall.zip](Challenge_files/basic_steganography/chall.zip)

# Solution

Before we start, note that the challenge description and name might be a bit misleading, as the solution isn't strictly related to steganography. This is just my opinion.

We got a compressed file `chall.zip` which was password protected.

Let's bruteforce it :3 using [John The Ripper](https://github.com/openwall/john)

```bash
zip2john chall.zip > hash.txt
ver 2.0 chall.zip/sap_ra_flag_roi_co_len.zip PKZIP Encr: cmplen=607943, decmplen=607931, crc=240795F6
john --incremental hash.txt | john --show hash.txt
[arch:95791] shmem: mmap: an error occurred while determining whether or not /tmp/ompi.arch.1000/jf.0/4188667904/shared_mem_cuda_pool.arch could be created.
[arch:95792] shmem: mmap: an error occurred while determining whether or not /tmp/ompi.arch.1000/jf.0/557907968/shared_mem_cuda_pool.arch could be created.
[arch:95791] create_and_attach: unable to create shared memory BTL coordinating structure :: size 134217728 
[arch:95792] create_and_attach: unable to create shared memory BTL coordinating structure :: size 134217728 
chall.zip/sap_ra_flag_roi_co_len.zip:chocolate:sap_ra_flag_roi_co_len.zip:chall.zip::chall.zip

1 password hash cracked, 0 left
Using default input encoding: UTF-8
```
Bingo! We got the password `chocolate`

Extract the file using the password, we got a directory called `chall`. 

Another compressed file was in the folder but it wasn't password protected, extract it give is a directory which has a image containing the flag.

```BKSEC{I_p4y_m4ss1v3_r3sp3ct_t0_th3_ppl_bu1ld1n9_th1s_club}```