---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434832"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет массив структур, описывающих именованные свойства, и проверяет их выделение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Параметры

 _Лппнамеид_
  
> возврата Указатель на массив структур [мапинамеид](mapinameid.md) , описывающих именованные свойства. 
    
 _записи cName_
  
> возврата Количество именованных структур свойств в массиве, на которое указывает параметр _лппнамеид_ . 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Одна или несколько указанных структур имени свойства являются недопустимыми. 
    
FALSE 
  
> Указаны допустимые структуры имени свойства.
    
## <a name="remarks"></a>Примечания

Функцию **фбадрглпнамеид** можно использовать при настройке вызова [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) или [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md). 
  

