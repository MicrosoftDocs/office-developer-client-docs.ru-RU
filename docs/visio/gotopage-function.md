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
description: Отображает страницу с именем страницы в активном окне.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302970"
---
# <a name="gotopage-function"></a>Функция GOTOPAGE

Отображает страницу с именем  *страницы*  в активном окне. 
  
## <a name="syntax"></a>Синтаксис

GOTOPAGE(" ** *pagename* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Обязательный  <br/> |**String** <br/> |Имя страницы, на которое нужно перейти.  <br/> |
   
## <a name="remarks"></a>Примечания

Если окно уже отображает страницу, это окно становится активным. Если  *имени страницы*  не существует, приложение пытается перейти к https://  *pagename*  /. Если Visio работает как сервер на месте, функция GOTOPAGE не влияет. 
  
Вы можете использовать функцию HYPERLINK для перемещения по любому пути DOS, UNC или URL-адреса. 
  
В более ранних версиях Visio эта функция отображается как _GOTOPAGE. Visio версии 4.0 и более поздние версии принимают любой стиль. 
  

