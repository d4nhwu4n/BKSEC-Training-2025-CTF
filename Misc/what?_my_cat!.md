# Challenge Description 
Hãy tìm toàn bộ thông tin có thể về chú mèo trong ảnh trên và sắp xếp vào trong flag dưới dạng:  

BKSEC{tên_mm/dd/yyyy(ngày sinh)_quốc gia_đồ ăn ưa thích}  

Lưu ý: nội dung trong flag là các ký tự viết thường  

Hint:
LSBUw6puIGNo4bupIGhvbmcgcGjhuqNpIHVzZXJuYW1lIG5oYSE== (base64)  
decode = (- Tên chứ hong phải username nha! )  

Ngoài ra thì, không phải Anh đâu hehe

![image](https://github.com/user-attachments/assets/7890cbdc-4698-4fd2-8251-1bd6036852a2)

# Solution
In the picture is spicyuuu, the challenge reffer to a cat so maybe we need to find info about her cat.  

Do a little research about her cat we could found a video of her talking about her cat.

https://www.tiktok.com/@spicyuuu/video/7188457011204443394?lang=en

After watching the video, we get the cat name is ```Gyoza```.  

https://en.namu.wiki/w/spicyuuu

In this website we get Gyoza's birthday is ```15th-December```. The tiktok video from the start is posted on 14-01-2023 and in the video Gyoza was 3 years old. So he was born in ```2019```

The hint said that Gyoza isnt from England, so we could assume he would take spicyuuu nationality - ```Singapore```.

On spicyuuu's instagram we could see a link to Gyoza's instagram. Browsing through his instagram we could find multiple picture of him taking picture a brand called ```ciao``` , must be his favourite food.

So we got ourself the flag

```BKSEC{gyoza_12/15/2019_singapore_ciao}```


