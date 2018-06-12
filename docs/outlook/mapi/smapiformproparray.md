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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812333"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Применимо к**: Outlook 
  
Содержит массив структур [SMAPIFormProp](smapiformprop.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанные макрос:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>Элементы

 **cProps**
  
> Число именованных свойств в массиве элементов **aFormProp** . 
    
 **ulPad**
  
>  Восемь байт внутренние поля, используемый для обеспечения правильного выравнивания. 
    
 **aFormProp**
  
> Массив, содержащий свойства формы.
    
## <a name="remarks"></a>Замечания

Структура **SMAPIFormPropArray** передается как параметр следующих методов: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>См. также



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Структуры MAPI](mapi-structures.md)

