---
title: Функция GOTOPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Отображает страницу с именем PageName в активном в текущий момент окне.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302970"
---
# <a name="gotopage-function"></a>Функция GOTOPAGE

Отображает страницу с именем *PageName* в активном в текущий момент окне. 
  
## <a name="syntax"></a>Синтаксис

GOTOPAGE ("* * *PageName* * *") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _PageName_ <br/> |Обязательный  <br/> |**String** <br/> |Имя страницы, на которую необходимо перейти.  <br/> |
   
## <a name="remarks"></a>Замечания

Если окно уже отображает страницу, это окно становится активным. Если *PageName* не существует, приложение пытается перейти в HTTPS:// *PageName* /. Если приложение Visio работает как сервер на месте, функция GOTOPAGE не оказывает никакого действия. 
  
С помощью функции HYPERLINK можно перейти к любому пути DOS, UNC или URL-АДРЕСу. 
  
В более ранних версиях продуктов Visio Эта функция отображается как _ГОТОПАЖЕ. Visio версии 4,0 и более поздних принимают любой из этих стилей. 
  

