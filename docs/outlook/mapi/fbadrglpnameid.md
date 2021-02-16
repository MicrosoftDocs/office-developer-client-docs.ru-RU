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
  
Проверяет массив структур, которые описывают именуемые свойства, и проверяет их выделение. 
  
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

 _lppNameId_
  
> [in] Указатель на массив структур [MAPINAMEID,](mapinameid.md) описывающих именуемые свойства. 
    
 _cNames_
  
> [in] Количество именуемой структуры свойств в массиве, на который указывает параметр _lppNameId._ 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Одна или несколько указанных структур имен свойств недопустимы. 
    
FALSE 
  
> Допустимы все указанные структуры имен свойств.
    
## <a name="remarks"></a>Примечания

Функцию **FBadRglpNameID** можно использовать при настройке вызова [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md) 
  

