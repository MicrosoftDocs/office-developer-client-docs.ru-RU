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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808444"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Применимо к**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lpRowSet_
  
> [in] Указатель на структуру [SRowSet](srowset.md) , идентифицирующий набор для проверки строк. Если указатель имеет значение NULL, структура является недопустимым. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Строки набора указанных строке является недопустимым или набор самого строк является недопустимым. 
    
FALSE 
  
> Строки набора указанной строки и набор самого строк являются допустимыми.
    
## <a name="see-also"></a>См. также



[FBadRow](fbadrow.md)

