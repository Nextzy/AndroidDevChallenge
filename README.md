# AndroidDevChallenge

### Objective
เขียนแอพดึงข้อมูลจาก Blogger โดยใช้ Blogger API เพื่อแสดงข้อมูลบนแอพแอนดรอยด์ โดยจะดึงข้อมูลบทความที่มีอยู่ในบล็อกๆหนึ่ง โดยจะแสดงภาพ Header และชื่อบทความของบล็อกนั้นๆ สามารถใช้ไลบรารีอะไรก็ได้ตามใจชอบ

###### Example
ถ้าบทความนั้นๆมีภาพ Header อยู่ด้วย ให้แสดงภาพซ้อนอยู่ข้างหลังแล้วมีชื่อบทความทับอยู่ข้างบน กรณีที่บทความนั้นไม่มีภาพ Header ให้แสดงชื่อบทความเพียงอย่างเดียว
![Example](https://raw.githubusercontent.com/Nextzy/AndroidDevChallenge/master/images/example.jpg)


###### Time limit
```
1 ชั่วโมง
```

###### Blogger API Key
```
AIzaSyBzL7-wKQl-bOHg7EyFxYrSWDrqIqGbt4Y
```

###### Blogger ID
```
2112378201659339351
```


### Reference

###### HTTP request
```
GET https://www.googleapis.com/blogger/v3/blogs/blogId/posts
```

###### Parameter
```
<<Required parameters>>
key           String         The API Key of the Blogger API.
blogId        String         The ID of the blog to fetch posts from.

<<Optional parameters>>
fetchBodies   Boolean        Whether the body content of posts is included (Use false)
fetchImages   Boolean        Whether image URL metadata for each post is included. (Use true)
maxResults    Integer        Maximum number of posts to fetch. (Use 30)
```

###### Sample Response
```json
{
    "kind": "blogger#postList",
    "nextPageToken": "CgkIHhjAo6mTgyoQ1-S7qYWZq6gd",
    "items": [
        {
            "kind": "blogger#post",
            "id": "2591053315335095630",
            "blog": {
                "id": "2112378201659339351"
            },
            "published": "2016-04-25T02:17:00+07:00",
            "updated": "2016-04-25T03:59:10+07:00",
            "etag": "\"GtyIIQmNmmUjEA0nwhSqMElCJ1g/dGltZXN0YW1wOiAxNDYxNTMxNTUwNzM4Cm9mZnNldDogMjUyMDAwMDAK\"",
            "url": "http://www.akexorcist.com/2016/04/what-is-multi-window-in-android-n-and-how-to-prepare-it.html",
            "selfLink": "https://www.googleapis.com/blogger/v3/blogs/2112378201659339351/posts/2591053315335095630",
            "title": "[Android Code] รู้จัก Multi Window บน Android N และวิธีการรับมือ",
            "images": [
                {
                    "url": "https://4.bp.blogspot.com/-qz1Qaf9sjIk/VxxgiOErARI/AAAAAAAA6QU/CyhdRwroUvQLr3bEIldUxWV4H9i05FfegCLcB/s1200/multi_window_in_android_n-header.jpg"
                }
            ],
            "author": {
                "id": "g114162000308411301557",
                "displayName": "Ake Exorcist",
                "url": "https://www.blogger.com/profile/15427271074457300336",
                "image": {
                    "url": "//lh5.googleusercontent.com/-8jmtqovK1gc/AAAAAAAAAAI/AAAAAAAA5ZM/AkbiWBmGXZ0/s35-c/photo.jpg"
                }
            },
            "replies": {
                "totalItems": "0",
                "selfLink": "https://www.googleapis.com/blogger/v3/blogs/2112378201659339351/posts/2591053315335095630/comments"
            },
            "labels": [
                "Android Code"
            ]
        },
        ...
    ],
    "etag": "\"GtyIIQmNmmUjEA0nwhSqMElCJ1g/MjAxNi0wNS0yNFQxNzowMzo0NC45MDZa\""
}
```


