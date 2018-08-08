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
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808404"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Относится к**: Outlook 
  
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

