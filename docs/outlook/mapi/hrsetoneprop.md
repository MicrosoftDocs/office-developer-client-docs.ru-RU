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
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589182"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет значение одного свойства в интерфейсе свойств, то есть интерфейс, полученный из [IMAPIProp.](imapipropiunknown.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameters

 _pmp_
  
> [in] Указатель на [интерфейс IMAPIProp,](imapipropiunknown.md) на котором должно быть установлено или изменено значение свойства. 
    
 _pprop_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) определяющий значение, запредельное для _свойства pmp._ 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

В отличие [от метода IMAPIProp::SetProps,](imapiprop-setprops.md) функция **HrSetOneProp** никогда не возвращает предупреждений. Так как оно задает только одно свойство, оно просто успешно или не удается. Для настройки или изменения нескольких свойств **SetProps быстрее.** 
  
Вы можете получить одно свойство с помощью [функции HrGetOneProp.](hrgetoneprop.md) 
  

