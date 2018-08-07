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
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808437"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Относится к**: Outlook 
  
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

