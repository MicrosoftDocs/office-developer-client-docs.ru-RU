---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588456"
---
# <a name="gender"></a>Gender

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает возможные значения для Пол обмена сообщениями пользователя.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>Members

 _genderMin_
  
> Минимальное количество различные значения, поддерживаемые для Пол.
    
 _genderUnspecified_
  
> Пол не задан для обмена сообщениями пользователя.
    
 _genderFemale_
  
> Пользователь, обмена мгновенными сообщениями, гнездо.
    
 _genderMale_
  
> Пользователь, обмена мгновенными сообщениями, штекер.
    
 _genderCount_
  
> Число различных значений, поддерживаемые для Пол.
    
 _genderMax_
  
> Максимальное число различные значения, поддерживаемые для Пол.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagGender](pidtaggender-canonical-property.md)

