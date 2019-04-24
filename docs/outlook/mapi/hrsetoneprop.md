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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347770"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет значение одного свойства для интерфейса свойства, то есть интерфейс, производный от [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Параметры

 _ПМП_
  
> возврата Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , для которого необходимо задать или изменить значение свойства. 
    
 _ппроп_
  
> возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую значение, которое должно быть задано для свойства _ПМП_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

В отличие от метода [IMAPIProp:: SetProps](imapiprop-setprops.md) , функция **хрсетонепроп** никогда не возвращает предупреждения. Так как задается только одно свойство, оно просто может быть успешным или неудачным. Для настройки или изменения нескольких свойств **SetProps** быстрее. 
  
Вы можете получить одно свойство с помощью функции [хржетонепроп](hrgetoneprop.md) . 
  

