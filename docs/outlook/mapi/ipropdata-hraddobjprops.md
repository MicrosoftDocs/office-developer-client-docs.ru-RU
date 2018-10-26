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
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591688"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавление одного или нескольких свойств типа PT_OBJECT объект.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно добавить.
    
 _lppProblems_
  
> [in, out] На вводимых пользователем данных, допустимый указатель на структуру [SPropProblemArray](spropproblemarray.md) , или значение NULL. В выходных данных, указатель указатель на структуру, которая содержит сведения о свойствах, которые не могут быть добавлены или значение NULL. Указатель на структуру массива проблема свойство возвращается только в том случае, если передается указатель допустимый. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно добавлены.
    
MAPI_E_INVALID_TYPE 
  
> Свойство введите, отличное от PT_OBJECT был передан в массиве, параметр _lpPropTagArray_ . 
    
MAPI_E_NO_ACCESS 
  
> Объект имеет значение не разрешать разрешение на чтение/запись.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Некоторые, но не для всех свойств были добавлены.
    
## <a name="remarks"></a>Замечания

Метод **IPropData::HrAddObjProps** добавляет одного или нескольких свойств типа PT_OBJECT к объекту. **HrAddObjProps** является альтернативой метод [IMAPIProp::SetProps](imapiprop-setprops.md) для свойства объекта, так как свойства объекта не могут создаваться путем вызова **SetProps**. Добавление свойства объекта результаты в тег свойства, в списке свойство теги, метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) возвращает. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если **HrAddObjProps** возвращает MAPI_W_PARTIAL_COMPLETION и установки _lppProblems_ допустимый указатель, проверяет, возвращенные структура [SPropProblemArray](spropproblemarray.md) для получения свойств, которые не были добавлены. Как правило только проблемы, возникающей — нехватка памяти. Бесплатная загрузка структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) , когда вы закончите с ним. 
  
Чтобы добавить свойство, целевой объект должен иметь разрешение на чтение/запись. Если **HrAddObjProps** возвращает MAPI_E_NO_ACCESS, так как он не позволяет изменять свойства нельзя добавить объект. Чтобы получить разрешение на чтение и запись в объект до вызова **HrAddObjProps**, вызовите [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) и установите для параметра _ulAccess_ значение IPROP_READWRITE. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

