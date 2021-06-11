---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416386"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет одно или несколько свойств типа PT_OBJECT объекту.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают свойства для добавления.
    
 _lppProblems_
  
> [in, out] При вводе допустимый указатель на [структуру SPropProblemArray](spropproblemarray.md) или NULL. На выходе указатель на указатель на структуру, содержаную сведения о свойствах, которые нельзя добавить, или NULL. Указатель на структуру массива проблем свойств возвращается только в том случае, если допустимый указатель передается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно добавлены.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства, помимо PT_OBJECT, был передан в массиве, на который указывает параметр _lpPropTagArray._ 
    
MAPI_E_NO_ACCESS 
  
> Установлено, что объект не разрешает разрешение на чтение и записи.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Некоторые, но не все свойства были добавлены.
    
## <a name="remarks"></a>Примечания

Метод **IPropData::HrAddObjProps** добавляет одно или несколько свойств типа PT_OBJECT объекту. **HrAddObjProps** предоставляет альтернативу методу [IMAPIProp::SetProps](imapiprop-setprops.md) для свойств объектов, так как свойства объектов невозможно создать с помощью вызова **SetProps.** Добавление свойства объекта приводит к включению тега свойств в список тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **hrAddObjProps** возвращает MAPI_W_PARTIAL_COMPLETION и вы задали  _lppProblems_ допустимый указатель, проверьте возвращенную структуру [SPropProblemArray,](spropproblemarray.md) чтобы узнать, какие свойства не были добавлены. Как правило, единственная проблема, которая возникает, это отсутствие памяти. Освободите **структуру SPropProblemArray,** назвав функцию [MAPIFreeBuffer](mapifreebuffer.md) после ее завершения. 
  
Чтобы добавить свойство, целевой объект должен иметь разрешение на чтение и записи. Если **hrAddObjProps** возвращает MAPI_E_NO_ACCESS, нельзя добавлять свойства к объекту, так как он не разрешает изменения. Чтобы получить разрешение на чтение и записи объекта перед вызовом **HrAddObjProps,** позвоните по телефону [IPropData::HrSetObjAccess и](ipropdata-hrsetobjaccess.md) установите параметр  _ulAccess_ в IPROP_READWRITE. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

