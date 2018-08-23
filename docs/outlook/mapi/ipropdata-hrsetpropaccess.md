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
ms.openlocfilehash: d0054e54d56fbe1cc6d6d783ffcd6330d8ab2e6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564663"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает уровень доступа или состояния для одной или нескольких свойств объекта.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно изменить. 
    
 _rgulAccess_
  
> [in] Массив битовой маски флаг. Каждый Битовая маска указывает уровни доступа или состояния или оба, для каждого свойства, определенный в массиве, параметр _lpPropTagArray_ . Двух массивов являются позиционные первого битовой маски в _rgulAccess_ описывает первого свойства, указывающий _lpPropTagArray_ , и т. д. Для каждого свойства tag можно задать один уровень доступа флаг и флаг одного состояния. В следующей таблице перечислены возможные флаги. 
    
|**Флаг уровня доступа**|**Состояние флага**|
|:-----|:-----|
|IPROP_READONLY, это означает, что свойство не может изменить  <br/> |IPROP_CLEAN, это означает, что свойство не были изменены.  <br/> |
|IPROP_READWRITE, это означает, что свойство может быть изменено.  <br/> |IPROP_DIRTY, это означает, что свойство были изменены.  <br/> |
   
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Флаги уровень доступа и состояние были успешно установлены.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка для задания свойства на объект только для чтения или объект, для которого вызывающий не имеет разрешений.
    
MAPI_E_INVALID_PARAMETER 
  
> Параметр _rgulAccess_ содержит недопустимое сочетание флаги, такие как IPROP_READONLY и IPROP_READWRITE. 
    
## <a name="remarks"></a>Замечания

Метод **IPropData::HrSetPropAccess** изменяет уровень доступа и состояние для свойств, которые определяются теги свойства в структуре [SPropTagArray](sproptagarray.md) указывает параметр _lpPropTagArray_ . Для каждого свойства существует соответствующие записи в массиве _rgulAccess_ . Операция может быть присвоено один флаг, указывающий, уровень доступа этого свойства, а другой флаг, указывающий, его состояние. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте **HrSetPropAccess** для определения при изменении значения отдельного свойства и изменить уровень доступа для одной или нескольких свойств объекта. 
  
## <a name="see-also"></a>См. также



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

