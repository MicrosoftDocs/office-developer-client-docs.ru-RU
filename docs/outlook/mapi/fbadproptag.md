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
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808416"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Относится к**: Outlook 
  
Проверяет тег указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> [in] Свойство tag для проверки.
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Тег указанное свойство не является допустимым тегом свойство MAPI. 
    
FALSE 
  
> Тег указанное свойство является допустимым тегом свойство MAPI.
    
## <a name="remarks"></a>Замечания

Функция **FBadPropTag** проверяет указанное свойство tag, на основе MAPI определений. Он сделать sures, тип свойства — это один из типов, определенных параметром MAPI, который идентификатор свойства определяется как этого типа. 
  
## <a name="see-also"></a>См. также



[FBadProp](fbadprop.md)

