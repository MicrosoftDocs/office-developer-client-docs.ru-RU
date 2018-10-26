---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d7886d08c21e8fff9aceb3437ecb6bbbd970ed7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591424"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает уровень доступа для объекта.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Параметры

 _ulAccess_
  
> [in] Битовая маска флаги, задающее уровень доступа объекта. Можно установить один из следующих флагов.
    
IPROP_READONLY 
  
> Задает объект уровень доступа только для чтения. 
    
IPROP_READWRITE 
  
> Задает объект уровень доступа для чтения и записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уровень доступа объекта был успешно установлен.
    
## <a name="remarks"></a>Замечания

Метод **IPropData::HrSetObjAccess** можно задать уровень доступа для объекта целиком, а не для отдельных свойств. **HrSetObjAccess** можно использовать для изменения уровня доступа, указанные при создании объекта. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы задать уровень доступа к свойству, вызовите **HrSetObjAccess** с флагом IPROP_READWRITE, задавать в параметре _ulAccess_ , чтобы сделать объект изменяемым. Затем вызовите метод [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , указав свойства конечного объекта в массиве указывает параметр _lpPropTagArray_ . 
  
Чтобы создать объект со свойствами, которые будут доступны только для чтения, чтобы клиенты, создайте объект чтения и записи, добавление необходимых свойств, а затем вызвать **HrSetObjAccess** для изменения объекта доступа только для чтения. 
  
Можно также использовать **HrSetObjAccess** чтобы предотвратить создание нового свойства клиентов. 
  
## <a name="see-also"></a>См. также



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

