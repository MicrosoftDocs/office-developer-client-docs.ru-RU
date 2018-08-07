---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809676"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Относится к**: Outlook 
  
Сравнивает два значения свойств, чтобы определить, является ли они равны. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValueA_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) определение первое значение свойства для сравнения. 
    
 _lpSPropValueB_
  
> [in] Указатель на структуру **SPropValue** определение второе значение свойства для сравнения. 
    
## <a name="return-value"></a>������������ ��������

 **LPropCompareProp** возвращает одно из следующих значений для большинства типов свойств: 
  
- Меньше нуля Если значение указанный в параметре параметр _lpSPropValueA_ меньше значения, указанного параметром _lpSPropValueB_ . 
    
- Больше нуля, если значение указанный в параметре _lpSPropValueA_ больше, чем, указанный в параметре _lpSPropValueB_.
    
- Ноль, если значение указанный в параметре _lpSPropValueA_ равно значению, указанный в параметре _lpSPropValueB_. 
    
Для типы свойств, которые имеют встроенные порядок не, такие как логическое значение или типы ошибок функция **LPropCompareProp** возвращает значение undefined, если два значения не равны. Это значение undefined значение отличное от нуля и согласованные вызовах. 
  
## <a name="remarks"></a>Замечания

Используйте функцию **LPropCompareProp** только в том случае, если типы два свойства, которые нужно сравнить, совпадают. 
  
До вызова метода **LPropCompareProp**, клиентское приложение или поставщик услуг необходимо сначала получить свойства для сравнения с помощью вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) . Когда вызовы клиента или поставщика **LPropCompareProp**, функция сначала проверяет тегов свойств, чтобы убедиться в том, сравнение значений свойств является допустимым. Функция затем сравнивает значения свойств, соответствующие значения. 
  
Если значения свойств не равны, **LPropCompareProp** определяет, какой из них более высокой версии. Свойства, которые сопоставлены **LPropCompareProp** нет необходимости принадлежащих на тот же объект. 
  

