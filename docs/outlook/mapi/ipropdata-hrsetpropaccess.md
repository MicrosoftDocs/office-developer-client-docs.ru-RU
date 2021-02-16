---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437856"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает уровень доступа или состояние для одного или более свойств объекта.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают изменимые свойства. 
    
 _rgulAccess_
  
> [in] Массив битовых заметок. Каждая битоваяmask указывает уровни доступа, состояние или оба свойства для каждого из свойств, указанных в массиве, на которое указывает параметр _lpPropTagArray._ Два массива являются позициональными, так как первая битоваяmask в  _rgulAccess_ описывает первое свойство, на которое  _указывает lpPropTagArray,_ и так далее. Для каждого тега свойства можно установить один флаг уровня доступа и один флаг состояния. В следующей таблице показаны возможные флаги. 
    
|**Флаг уровня доступа**|**Флаг состояния**|
|:-----|:-----|
|IPROP_READONLY, что указывает на то, что свойство не может быть изменено  <br/> |IPROP_CLEAN, что указывает на то, что свойство не было изменено.  <br/> |
|IPROP_READWRITE, что указывает на то, что свойство можно изменить.  <br/> |IPROP_DIRTY, что указывает на то, что свойство было изменено.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Флаги уровня доступа и состояния успешно установлены.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка установить свойство для объекта, доступного только для чтения, или объекта, для которого у вызываемого объекта недостаточно разрешений.
    
MAPI_E_INVALID_PARAMETER 
  
> Параметр  _rgulAccess_ содержит недопустимое сочетание флагов, например IPROP_READONLY и IPROP_READWRITE. 
    
## <a name="remarks"></a>Примечания

Метод **IPropData::HrSetPropAccess** изменяет уровень доступа и состояние свойств, которые определены тегами свойств в структуре [SPropTagArray,](sproptagarray.md) на которые указывает параметр _lpPropTagArray._ Для каждого свойства в массиве  _rgulAccess_ есть соответствующая запись. Для записи можно установить один флаг, который указывает уровень доступа свойства, а другой флаг, который указывает его состояние. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте **HrSetPropAccess,** чтобы определить, когда изменяется определенное значение свойства, и изменить уровень доступа для одного или более свойств объекта. 
  
## <a name="see-also"></a>См. также



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

