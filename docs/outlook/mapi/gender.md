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
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808531"
---
# <a name="gender"></a>Gender

  
  
**Относится к**: Outlook 
  
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

