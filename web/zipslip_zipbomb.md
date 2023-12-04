---
layout: post
title: Zip Slip & Zip Bomb
subtitle: zip 파일 업로드 공격 시나리오
---

파일 업로드 기능이 존재하는 서비스를 진단하다보면 Server-side Language 유형의 파일을 업로드가 불가능한 경우가 존재한다.
이러한 경우 허용되고 있는 파일 유형을 통한 공격 가능성을 살펴보게 되는데, 이번 포스팅에서는 zip 파일 업로드가 허용된 경우에 발생 가능한 공격 시나리오를 살펴보려고한다.

업로드 기능에서 zip 파일이 허용되고 있지만 zip 파일에 대한 검증이 부재/미흡한 경우에는 Zip Slip 또는 Zip Bomb과 같은 공격이 가능하다.

##Zip Slip

