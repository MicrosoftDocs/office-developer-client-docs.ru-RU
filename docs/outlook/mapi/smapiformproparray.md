---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420068"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [SMAPIFormProp.](smapiformprop.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанный макрос:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>"Участники"

 **cProps**
  
> Количество именуемых свойств в массиве **в члене aFormProp.** 
    
 **ulPad**
  
>  Восемь байт заполнения, используемого для обеспечения правильного выравнивания. 
    
 **aFormProp**
  
> Массив свойств формы.
    
## <a name="remarks"></a>Примечания

Структура **SMAPIFormPropArray** передается в качестве параметра следующим методам: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>См. также



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Структуры MAPI](mapi-structures.md)

