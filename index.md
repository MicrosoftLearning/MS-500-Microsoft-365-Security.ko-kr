---
title: 온라인 호스팅 지침
permalink: index.html
layout: home
ms.openlocfilehash: f4e2e1489e1997cfd064aa74eb5345e302bb2424
ms.sourcegitcommit: c203d5d5aaaf93bae4a8af2ae04b27f6314242c4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/13/2021
ms.locfileid: "137821085"
---
# <a name="content-directory"></a>콘텐츠 디렉터리

다음은 각 랩 연습 및 데모의 하이퍼링크입니다.

## <a name="labs"></a>랩

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| 모듈 | 랩 |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## <a name="demos"></a>데모

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" %}
| 모듈 | 데모 |
| --- | --- | 
{% for activity in demos  %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
