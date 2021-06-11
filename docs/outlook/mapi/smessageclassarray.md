---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412697"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив указателей для строк класса сообщений.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанный макрос:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество указателей строки класса сообщений в массиве.
    
 **aMessageClass**
  
> Массив указателей для строк класса сообщений.
    
## <a name="remarks"></a>Примечания

Структура **SMessageClassArray** передается в качестве параметра в следующих методах: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

