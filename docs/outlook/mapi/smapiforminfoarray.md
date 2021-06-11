---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416974"
---
# <a name="smapiforminfoarray"></a>SMAPIFormInfoArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив указателей для формирования информационных объектов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанный макрос:  <br/> |[CbMAPIFormInfoArray](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a>"Участники"

 **cForms**
  
> Количество указателей в массиве, на который указывает **член aFormInfo.** 
    
 **aFormInfo**
  
> Указатель на массив указателей для формирования информационных объектов.
    
## <a name="remarks"></a>Примечания

Структура **SMAPIFormInfoArray** передается в качестве параметра в следующих методах: 
  
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormMgr::SelectMultipleForms](imapiformmgr-selectmultipleforms.md)
    
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

