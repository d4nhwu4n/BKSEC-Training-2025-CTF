# Challenge description 
Cuối cùng cũng đã bắt được tên tội phạm anhtvie. Sau màn thẩm vấn không mấy thành công, chúng tôi đã phải chuốc rượu hắn để bắt hắn nói ra cờ. Trong cơn say, chúng tôi chỉ lấy được một bức ảnh, và hắn thì cứ luôn miệng nói "WHEREMYFLAG" khiến chúng tôi chẳng biết làm gì nữa. Bạn có thể giúp chúng tôi lấy được cờ không?

File given: [Where_my_flag.jpg](Challenge_files/Drunken_flag/Where_my_flag.jpg)

# Solution
We received an image that appears empty upon opening. It is possible that the flag is hidden within the image.

We can use a tool called `steghide` to check if there is any hidden data in the image.

```bash
steghide extract -sf Where_my_flag.jpg
Enter passphrase: 
wrote extracted data to "Flag.rar".
```

BINGO! We extracted `Flag.rar` from the image using `steghide` with the passphrase `WHEREMYFLAG`.

However, `Flag.rar` isn't a RAR file. Strange!

Opening `Flag.rar` with a hex editor, we notice that the file's [magic bytes](https://en.wikipedia.org/wiki/List_of_file_signatures) do not match those of a .rar file.

Let's edit the hex to make the file a REAL .RAR file by editing the magic bytes to `52 61 72 21 1A 07 01 00`

Now we can open the .RAR file which contains a Flag.txt

The Flag.txt contain multiple lines of python code. After reading and re-write it, we got the following encoded text.

```python 
flag_parts = [
    "6H8WNA+N841BS",
    "A622CW56/1CCA6",
    "23C.1CVJEQPCGM",
    "6E2CV59SPEZ2"
]

encoded = ''.join(flag_parts)
print(f"Encoded: {encoded}")
```
It will give us: `6H8WNA+N841BSA622CW56/1CCA623C.1CVJEQPCGM6E2CV59SPEZ2`

We could use [CyberChef](https://gchq.github.io/CyberChef/) to decode the text.

We got the flag.

```BKSEC{W41T_H0w_D1D_u_Cr4ck3d_TH1s?}```

