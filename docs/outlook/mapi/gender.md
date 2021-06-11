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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428650"
---
# <a name="gender"></a>Gender

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает возможные значения для пола пользователя обмена сообщениями.
  
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

## <a name="members"></a>Элементы

 _genderMin_
  
> Минимальное количество различных значений, поддерживаемых для пола.
    
 _genderUnspecified_
  
> Пол пользователя обмена сообщениями не указывается.
    
 _genderFemale_
  
> Пользователь обмена сообщениями — женщина.
    
 _genderMale_
  
> Пользователь обмена сообщениями — мужчина.
    
 _genderCount_
  
> Количество различных значений, поддерживаемых для пола.
    
 _genderMax_
  
> Максимальное количество различных значений, поддерживаемых для пола.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagGender](pidtaggender-canonical-property.md)

