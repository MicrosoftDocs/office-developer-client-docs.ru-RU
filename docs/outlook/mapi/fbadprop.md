---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578852"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Проверяет указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Параметры

 _lpprop_
  
> [in] Структура [SPropValue](spropvalue.md) , определение свойства для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Указанное свойство является недопустимым. 
    
FALSE 
  
> Указанное свойство является допустимым.
    
## <a name="remarks"></a>Замечания

Поставщик службы можно вызвать функцию **FBadProp** по ряду причин, например подготовить для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) , задав свойство. **FBadProp** проверяет указанное свойство в зависимости от типа свойства. Например, если свойство имеет логическое значение, **FBadProp** сделать sures, что его значением является либо TRUE или FALSE. Если свойство имеет двоичный, **FBadProp** проверяет его указатель и размер и следит за тем, что он правильно выделенное. 
  
## <a name="see-also"></a>См. также



[FBadPropTag](fbadproptag.md)

