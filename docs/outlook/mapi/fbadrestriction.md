---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432242"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет ограничение, используемое для ограничения представления таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Параметры

 _лпрес_
  
> возврата Структура [срестриктион](srestriction.md) , определяющая ограничение, которое необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанное ограничение или один или несколько его подограничений являются недопустимыми. 
    
FALSE 
  
> Указанное ограничение и все его подограничения действительны.
    
## <a name="remarks"></a>Примечания

После проверки ограничения его можно передать в вызовах метода [IMAPITable:: restrict](imapitable-restrict.md) , чтобы ограничить таблицу определенными строками, на метод [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения строки таблицы, а также методы интерфейса [IMAPIContainer](imapicontainerimapiprop.md) для выполнения ограничения для объекта Container. 
  

