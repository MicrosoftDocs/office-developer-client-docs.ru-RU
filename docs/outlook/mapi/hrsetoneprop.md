---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417660"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет значение одного свойства интерфейса свойства, то есть интерфейса, производного от [IMAPIProp.](imapipropiunknown.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Параметры

 _pmp_
  
> [in] Указатель на интерфейс [IMAPIProp,](imapipropiunknown.md) для которого необходимо установить или изменить значение свойства. 
    
 _pprop_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) определяющий значение, заносяющееся в _свойство PMP._ 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

В отличие от метода [IMAPIProp::SetProps](imapiprop-setprops.md) функция **HrSetOneProp** никогда не возвращает предупреждений. Так как задает только одно свойство, оно просто будет успешным или неудачным. Для настройки или изменения нескольких свойств **SetProps быстрее.** 
  
Можно получить одно свойство с помощью функции [HrGetOneProp.](hrgetoneprop.md) 
  

