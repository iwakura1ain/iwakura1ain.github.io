---
title: Forum Video Maker
layout: project
type: cli
desc: Reddit 댓글들을 크롤링한 후 유투브 영상으로 조합하는 프로그램
categories: cli python selenium crawling youtube
repo: https://github.com/iwakura1ain/forum-video-maker
live: https://www.youtube.com/playlist?list=PLRHUNQ32SoCL2vknJkh5J91F2FszwYJgr
---


# 개요

**Reddit 댓글들을 크롤링 해 영상으로 만드는 프로그램**

{% include stack.html %}


## 인원과 역할

-   개인프로젝트


# 프로젝트


## Reddit에서 포스팅을 자동으로 크롤링

-   **Selenium** 을 사용해서 Reddit 댓글 **내용과 사진 캡쳐**
-   중복된 댓글은 sqlite3에 해시 저장 후 무시

![img](./videomaker-db.png)


## 포스팅 대사와 배경 영상 조합

-   구글 TTS API 사용해 **대사 생성**
-   moviepy 사용해 **영상 생성**

![img](./videomaker-video.png)


## 유투브에 자동 업로드

-   유투브 API 사용해 개인 계정에 업로드

![img](./videomaker-upload.png)


# 제한사항
