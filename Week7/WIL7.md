# WEEK7

[https://binary-ho.notion.site/7-1c9d44ab9867474fb2bcdb750ecd746e](https://www.notion.so/1c9d44ab9867474fb2bcdb750ecd746e)

[https://www.notion.so/WEEK7-c5c82557f81e489a8da94969af78b965?pvs=4](https://www.notion.so/WEEK7-c5c82557f81e489a8da94969af78b965)

index.html

```html
<!doctype html>

<html Lang="en">

<head>

    <meta charset="utf-8">
    <meta name = "viewport" contest="width=device-width, initial-scale=1">
    <link rel = "stylesheet" href = "style.css">
    <title>유튜브 클론 HTML</title>
    
</head>

<body>

    <!-- 헤더 -->
    <div id="header" class="flex-row-space-between">
        
        <!-- 로고와 햄버거 버튼이 있는 부분 -->
        <div class="flex-row-center">
            <div class="grey-bakcground">🍔</div>
            <div class="pointer" style="font-weight: bold; margin-left: 30px;">GDSC</div>
        </div>
        
        <!-- 검색 바 -->
        <div class="flex-row-center" style="margin: 5px;">
            <div id="search-bar">
                <input style="width: 93%; border: none;" placeholder="검색" />
                <div class="pointer" style="background-color: white; border: none;">🔍</div>
            </div>  
            <div class="grey-bakcground">🎤 </div>
        </div>

        <!-- 버튼과 프로필 사진이 있는 부분 -->
        <div class="flex-row-center">
            <div class="grey-bakcground">📽 </div>
            <div class="grey-bakcground">🔔</div>
            <div class="grey-bakcground">💩</div>
        </div>
        
    </div>

    

    <div id = "aside-container">
        <div id="aside-container-inner" class="style">
                
    </div>    

    <div id = "video-container">
        <img class = "profile-thumbnail"
            src = "C:\Users\Administrator\Desktop\CLONEYOUTUBE">
    </div>

    <div id="video-info-container">
        <h1>[충격, 공포] GDSC의 충격적인 실체.....</h1>
            <div class="flex-row-space-between">
                <div id="creater-container">
                    <img class="profile-thumbnail"
                        src="https://user-images.githubusercontent.com/71186266/222961900-8528af30-d286-460d-b36c-91b11c8caa34.png" />
                    <div class="flex-column" style="margin: 5px;">
                        <p style="font-size: 15px; font-weight: bold; margin: 5px;">고라니맨</p>
                        <p style="font-size: 10px; margin: 5px;">구독자 5억명</p>
                    </div>

                    <div class="dropdown flex-column">
                        <span class="grey-button">🔔 구독중</span>
                        <div class="dropdown-box" style="width: 100%">
                            <a class="dropdown-content"> 🔔 전체 </a>
                            <a class="dropdown-content"> 🛎 맞춤설정 </a>
                            <a class="dropdown-content"> 🔕 없음 </a>
                            <a class="dropdown-content"> 😭 손절하기 </a>
                        </div>
                    </div>
                </div>

                <div class="flex-row-center">
                    <div class="grey-button">👍 10억 | 👎</div>
                    <div class="grey-button flex-column">↗ 공유
                        <div class="description">
                            <a>공유하기</a>
                        </div>
                    </div>

                    <div class="grey-button flex-column"> 🔽 오프라인 저장
                        <div class="description">
                            <a>오프라인 저장</a>
                        </div>
                    </div>
        
                    <div class="grey-button flex-column"> ❤ Thanks
                        <div class="description flex-column">
                            <a>Super Thanks로 응원하는 마음을 표현하세요 </a>
                        </div>
                    </div>

                    <div class="grey-button flex-column">✂ 클립
                        <div class="description">
                            <a>클립</a>
                        </div>
                    </div>
                   
                    <div class="grey-button">...</div>
                </div>
            </div>

            <div class="grey-button" style="width: 95%;">
                <div>GDSC는 사실 XXX다?</div>
                <div>정보들..</div>
                <div>정보들..</div>
            </div>
        </div>

        
        <div class="flex-row-space-between">
            <div id="creater-container">
                <img class="profile-thumbnail"
                    src="https://user-images.githubusercontent.com/71186266/222961900-8528af30-d286-460d-b36c-91b11c8caa34.png" />
                
                <div class="flex-column" style="margin: 5px;">
                    <p style="font-size: 15px; font-weight: bold; margin: 5px;">고라니맨</p>
                    <p style="font-size: 10px; margin: 5px;">구독자 5억명</p>
                </div>

                <div class="dropdown flex-column">
                    <span class="grey-button">🔔 구독중</span>
                    <div class="dropdown-box" style="width: 100%">
                        <a class="dropdown-content"> 🔔 전체 </a>
                        <a class="dropdown-content"> 🛎 맞춤설정 </a>
                        <a class="dropdown-content"> 🔕 없음 </a>
                        <a class="dropdown-content"> 😭 손절하기 </a>
                    </div>
                </div>
            </div>    

            <div class="flex-column" style="margin: 5px;">
                <p style="font-size: 15px; font-weight: bold; margin: 5px;">고라니맨</p>
                <p style="font-size: 10px; margin: 5px;">구독자 5억명</p>
            </div>

            <div class="dropdown">
                <span class="grey-button">🔔 구독중</span>
                <div class="dropdown-box" style="width: 100%;">
                    <a class="dropdown-content"> 🔔 전체 </a>
                    <a class="dropdown-content"> 🛎 맞춤설정 </a>
                    <a class="dropdown-content"> 🔕 없음 </a>
                    <a class="dropdown-content"> 😭 손절하기 </a>
                </div>
            </div>
    </div>

            
    <div id = "comment-container">
                <!-- 댓글 입력 -->
        <div class="comment-input-box">
            <img class="profile-thumbnail"
                src="https://user-images.githubusercontent.com/71186266/222961900-8528af30-d286-460d-b36c-91b11c8caa34.png" />
            <input
                style="height: 25px; width: 90%; border-top: none; border-left: none; border-right: none; border-bottom: 1px solid; margin: 20"
                placeholder="댓글 추가...">
        </div>

        <div class="comment-box">
            <img class="profile-thumbnail"
            src="https://user-images.githubusercontent.com/71186266/222961900-8528af30-d286-460d-b36c-91b11c8caa34.png" />
        
        <div class="comment-text-area">
            <div style="font-weight: bold;"> 고라니 </div>
            <div>GDSC! GDSC! GDSC! GDSC!</div>
            <div class="like-hate-area">
                <div>👍</div>
                <div>1m</div>
                <div>👎</div>
            </div>
        </div>
    </div>

</body>

</html>
```

style.css

```css
@import 'reset.css';

#header {
  position: sticky;
  top: 0;
  padding: 0px 30px;

  background-color: white;
}

.flex-row-space-between {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.flex-row-center {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.flex-column {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.grey-bakcground {
  margin: 10px;
  padding: 10px;
  border-radius: 50%;
}

.grey-bakcground:hover {
  background-color: grey;
  cursor: pointer;
}

.pointer:hover {
  cursor: pointer;
}

#search-bar {
  width: 450px;
  border: 3px solid grey;
  border-radius: 20px;
  padding: 5px 10px;
  color: grey;
  display: flex;
  flex-direction: row;
}

#container {
  display: flex;
  flex-direction: row;
  background-color: white;
  margin: 50px;
}

#main-container {
  width: 70vw;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

#video-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  margin: 50px;
}

#video-info-container {
  display: flex;
  flex-direction: column;
}

#creater-container {
  display: flex;
  flex-direction: row;
  align-items: center;
}

#comment-container {}

.comment-box {
  display: flex;
  flex-direction: row;
  margin: 10px;
}

.comment-text-area {
  display: flex;
  flex-direction: column;
}

.comment-input-box {
  display: flex;
  flex-direction: row;
  margin: 10px;
  align-items: center;
}

.profile-thumbnail {
  width: 50px;
  height: 50px;
  margin: 5px;
  border-radius: 25px;
}

.like-hate-area {
  display: flex;
  flex-direction: row;
}

.grey-button {
  background-color: whitesmoke;
  border-radius: 25px;
  padding: 15px;
  margin: 10px;
}

.grey-button:hover {
  background-color: lightgray;
  cursor: pointer;
}

.grey-button {
  background-color: whitesmoke;
  border-radius: 25px;
  padding: 15px;
  margin: 10px;
}

.grey-button:hover {
  background-color: lightgray;
  cursor: pointer;
}

.description {
  display: none;
  position: absolute;
  margin-top: 40px;
  z-index: 1;
}

.grey-button:hover .description {
  display: block;
}

.description a {
  display: block;
  color: white;
  background-color: black;
  padding: 10px;
}

/* 드롭다운 */
.dropdown {
  position: relative;
}

.dropdown:hover .dropdown-box {
  display: block;
}

.dropdown-box {
  display: none;
  position: absolute;
  padding: 10px;
  margin-top: 60px;

  z-index: 1;
}

.dropdown-box a {
  display: block;
}

.dropdown-content {
  background-color: whitesmoke;
  padding: 15px;
}

.dropdown-content:hover {
  background-color: lightgray;
  cursor: pointer;
}

input:focus {
  outline: none;
}
```

reset.css

```css
html, body, div, span, applet, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr, acronym, address, big, cite, code, del, dfn, em, img, ins, kbd, q,s,samp, small, strike, strong, sub, tt, var, b,u, i, center, dl, dt,dd, ol, ul, li, fieldset, form, label, legend, table, caption, tbody, tfoot, thead, tr, th, td, article, aside, canvas, details, embed, figure, figcaption, footer, header, hgroup, menu, nav, output, ruby, section, summary, time, mark, audio, video { 
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
}

/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, footer, header, hgroup, menu, nav, section {
    display: block;
}

body {
line-height: 1;
}

ol, ul {
list-style: none;
}

blockquote, q {
quotes: none;
}

blockquote:before, blockquote:after, q:before, q:after {
content: '';
content: none;
}

table { border-collapse: collapse; border-spacing: 0;
}
```
