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
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425157"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает уровень доступа для объекта.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Parameters

 _ulAccess_
  
> [in] Битмашка флагов, которая указывает уровень доступа объекта. Можно установить один из следующих флагов:
    
IPROP_READONLY 
  
> Задает уровень доступа объекта только для чтения. 
    
IPROP_READWRITE 
  
> Задает уровень доступа объекта для чтения и записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уровень доступа объекта был успешно установлен.
    
## <a name="remarks"></a>Примечания

Метод **IPropData::HrSetObjAccess задает** уровень доступа для всего объекта, а не для отдельных свойств. **HrSetObjAccess можно** использовать для изменения уровня доступа, установленного при создания объекта. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы установить уровень доступа к свойству, сначала позвоните **в HrSetObjAccess** с флагом IPROP_READWRITE в параметре  _ulAccess,_ чтобы сделать объект модификабельным. Затем позвоните в [метод IPropData::HrSetPropAccess,](ipropdata-hrsetpropaccess.md) указав целевое свойство в массиве, на который указывает параметр _lpPropTagArray._ 
  
Чтобы создать объект с свойствами, которые будут доступны только для чтения клиентам, создайте объект read/write, добавьте необходимые свойства, а затем позвоните **в HrSetObjAccess,** чтобы изменить доступ объекта к только для чтения. 
  
Вы также можете использовать **HrSetObjAccess,** чтобы предотвратить создание клиентами новых свойств. 
  
## <a name="see-also"></a>См. также



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

