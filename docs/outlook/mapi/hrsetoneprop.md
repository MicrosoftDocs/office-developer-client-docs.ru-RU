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
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569129"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет значения одного свойства для интерфейса свойство, то есть, производные от [IMAPIProp](imapipropiunknown.md)интерфейс. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Параметры

 _pmp_
  
> [in] Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , где значение свойства — установить или изменить. 
    
 _pprop_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) , определяющий значение должно быть задано для свойства _pmp_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

В отличие от метода [IMAPIProp::SetProps](imapiprop-setprops.md) функция **HrSetOneProp** никогда не возвращает все предупреждения. Так как только одно свойство, он просто либо успешного или неудачного завершения. Для параметра или изменение значений нескольких свойств **SetProps** выполняется быстрее. 
  
Вы можете получить отдельное свойство с помощью функции [HrGetOneProp](hrgetoneprop.md) . 
  

