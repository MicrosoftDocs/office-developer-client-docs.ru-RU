---
title: Функция NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Возвращает значение истина (1), если логикалекспрессион имеет значение FALSE. В противном случае возвращается значение FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341141"
---
# <a name="not-function"></a>Функция NOT

Возвращает значение истина (1), если _логикалекспрессион_ имеет значение false. В противном случае возвращается значение FALSE (0). 
  
## <a name="syntax"></a>Синтаксис

НЕТ (* * *логикалекспрессион* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _логикалекспрессион_ <br/> |Обязательный  <br/> |**String** <br/> |Логическое выражение для оценки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="example"></a>Пример

НЕТ (высота \> 0,75) 
  
Возвращает 1, если высота меньше или равна 0,75 сантиметра. Возвращает значение 0, если высота превышает 0,75 дюймов. 
  

