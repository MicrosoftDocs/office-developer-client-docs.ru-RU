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
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341008"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет допустимость набора столбцов таблицы для использования поставщиком услуг при следующем вызове метода [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Параметры

 _Лпптаколс_
  
> возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, определяющих столбцы таблицы, которые необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указан недопустимый набор столбцов. 
    
FALSE 
  
> Указанный набор столбцов является допустимым.
    
## <a name="remarks"></a>Комментарии

Функция **фбадколумнсет** обрабатывает столбцы типа пт_еррор как недопустимые и столбцы типа пт_нулл как допустимые. 
  

