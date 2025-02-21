# Challenge Description
Where am I?

Các bạn cần tìm ra:

Địa điểm đang được chụp có tên là gì (dựa theo Google Maps Tiếng Việt)

Con đường mà tôi đang hướng đến có tên là gì?

Tổng số Pixel có trong bức ảnh.

Các thông tin trên được viết liền, không dấu, viết thường.

Ví dụ về flag: BKSEC{daihocbachkhoahanoi_daicoviet_13371337}

File given: [chall.zip](/Challenge_files/langthanghanoi/chall.zip)
# Solution
We got a zip file from the challenge, let's extract it and see what's inside.

We got a image file named 'challenge.jpeg'. 

Inpsecting the image give us nothing.

We could try to look at the image metadata too see where the image was taken as well as the size of the image.

```bash
exiftool challenge.jpeg
```

![image](https://github.com/user-attachments/assets/d7535a6f-8707-4c1c-891e-f31bc9049a82)

Bingo we got the location coordinates.

Using Google Maps we could find the location and the road we need to find.

![image](https://github.com/user-attachments/assets/fa0fbc33-a0c0-4af0-aac6-b1b5096ccffa)

So the in the picture was the ```CharmVit Tower``` and the road was ```Hoang Minh Giam```

![image](https://github.com/user-attachments/assets/1c91b462-bf00-44aa-9311-086aee845930)

The picture size was 1536x2048 which equivalent to ```3145728``` pixels.

We got the flag

```BKSEC{charmvittower_hoangminhgiam_3145728}```
