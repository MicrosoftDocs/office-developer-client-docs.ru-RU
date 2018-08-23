---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590962"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Проверяет все строки в таблице, включенных в набор строк таблицы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Параметры

 _lpRowSet_
  
> [in] Указатель на структуру [SRowSet](srowset.md) , идентифицирующий набор для проверки строк. Если указатель имеет значение NULL, структура является недопустимым. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Строки набора указанных строке является недопустимым или набор самого строк является недопустимым. 
    
FALSE 
  
> Строки набора указанной строки и набор самого строк являются допустимыми.
    
## <a name="see-also"></a>См. также



[FBadRow](fbadrow.md)

