---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590164"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Проверяет строку в таблице.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Параметры

 _lprow_
  
> [in] Указатель на структуру [SRow](srow.md) , идентифицирующий строку для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Указанная строка является недопустимым.
    
FALSE 
  
> Указанная строка является допустимым.
    
## <a name="see-also"></a>См. также



[FBadRowSet](fbadrowset.md)

