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
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575100"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  

