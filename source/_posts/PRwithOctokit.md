---
title: Making Pull Request with Octokit Library
date: 2021-07-28 11:10:49
categories: Github
tags: Github, PR, 'Pull request', github api, Octokit, 'Octokit Library'
---


## 이 글을 읽기 전에..
Octokit 라이브러리와 Pull Request가 무엇인지 궁금할 경우
[지난 포스트](https://dblepart99.github.io/2021/07/28/What-is-Pull-Request/)를 확인해보시면 됩니다.

<br/>

## Octokit Library로 Pull Request생성하기

``` javascript
const { Octokit } = require("@octokit/core");

const octokit = new Octokit({
    auth: token // B의 토큰
});

 async function makePRfromAtoB(){       // B의 레포를 fork한 후 A가 수정하여 PR을 날리는 경우
     await octokit.request("POST /repos/{owner}/{repo}/pulls", {
         owner: "binaryKim99",         // 풀리퀘 받을 학생 이름 -> B
         title: "PR title",            // 풀리퀘 제목 
         repo: "binaryKim99Resume",    // 풀리퀘 날릴 레포 이름
         body: "pull request body",    // 풀리퀘 관련 내용 
         head: "CNUCSE-RESUME:main",   //A의 이름:branch 이름
         base: "main",                 //B의 branch 이름
     });
     
 }
 
 makePRfromAtoB();
```