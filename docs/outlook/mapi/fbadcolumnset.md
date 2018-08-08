---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808420"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Относится к**: Outlook 
  
Тестов, задайте действия столбец таблицы для использования поставщиком услуг в последующих вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Параметры

 _lpptaCols_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, определение столбцов в таблице для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Недопустимый набор указанного столбца. 
    
FALSE 
  
> Набор указанного столбца является допустимым.
    
## <a name="remarks"></a>Замечания

Функция **FBadColumnSet** обрабатывает столбцы типа PT_ERROR как недопустимый и столбцы типа PT_NULL действительным. 
  

