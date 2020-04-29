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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434720"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

 _лпптаколс_
  
> возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, определяющих столбцы таблицы, которые необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указан недопустимый набор столбцов. 
    
FALSE 
  
> Указанный набор столбцов является допустимым.
    
## <a name="remarks"></a>Примечания

Функция **фбадколумнсет** обрабатывает столбцы типа PT_ERROR как недопустимые и столбцы типа PT_NULL как допустимые. 
  

