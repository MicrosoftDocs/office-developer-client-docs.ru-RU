---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433649"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет указанный тег свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _улпроптаг_
  
> возврата Тег свойства, который необходимо проверить.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанный тег свойства не является допустимым тегом свойства MAPI. 
    
FALSE 
  
> Указанный тег свойства является допустимым тегом свойства MAPI.
    
## <a name="remarks"></a>Примечания

Функция **фбадпроптаг** проверяет заданный тег свойства на основе определений MAPI. Он гарантирует, что тип свойства является одним из типов, определенных MAPI, и что идентификатор свойства определен как тип этого типа. 
  
## <a name="see-also"></a>См. также



[FBadProp](fbadprop.md)

