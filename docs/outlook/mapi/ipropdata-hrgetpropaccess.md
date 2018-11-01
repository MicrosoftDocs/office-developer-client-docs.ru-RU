---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64b0c0501a6ef4471f97e82b231ef430681f1306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573392"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает уровень доступа и состояние для одной или нескольких свойств объекта.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Параметры

 _lppPropTagArray_
  
> [in, out] На входе массив тегов свойств, которые указывают свойства, для которого нужно извлечь уровни доступа и состоянии; в противном случае указатель на значение NULL, это означает, что **HrGetPropAccess** следует извлечь уровни доступа и состояние для всех свойств. На выходе были извлечены массив теги свойства для каких флаги доступа и состояние. Флаги хранятся в массиве указывает параметр _lprgulAccess_ . 
    
 _lprgulAccess_
  
> [out] Указатель на массив битовой маски флаг. Каждый Битовая маска указывает уровни доступа или состояния или оба, для каждого из свойств, указанных в массиве указывает параметр _lpPropTagArray_ . Двух массивов являются позиционные первого Битовая маска, указывающая, что _lprgulAccess_ моменты, которые описываются первого свойства, _lpPropTagArray_ указывает, и т. д. Для каждого свойства tag можно задать следующие флажки: 
    
|**Флаг уровня доступа**|**Состояние флага**|
|:-----|:-----|
|IPROP_READONLY, это означает, что свойство не подлежит изменению.  <br/> |IPROP_CLEAN, это означает, что свойство не были изменены.  <br/> |
|IPROP_READWRITE, это означает, что свойство может быть изменено.  <br/> |IPROP_DIRTY, это означает, что свойство были изменены.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Флаги состояние и уровень доступа для свойств были успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IPropData::HrGetPropAccess** получает набор флагов, которое указывает, уровень доступа и состояние для одного или нескольких свойств. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих объектов:

**HrGetPropAccess** можно использовать в следующих целях: 
  
- Чтобы определить ли это клиент, изменения или удаления для записи свойств.
    
- Чтобы клиент не изменять или удалять свойства с помощью методов [IMAPIProp](imapipropiunknown.md) . 
    
Если одно из свойств в массиве тег свойства, на который указывает _lppPropTagArray_ была удалена, **HrGetPropAccess** задает запись массива 0 для вывода. Если _lppPropTagArray_ значение NULL и одно из свойств объекта был удален, удаленные свойство возвращается в массиве. 
  
Если свойство был изменен, его IPROP_DIRTY флаг имеет значение в соответствующей записи в массиве, указывающий _lprgulAccess_ . Будет установлено ни IPROP_READONLY, ни IPROP_READWRITE. 
  
Если свойство не были изменены или удалены, будет установлен только флаг IPROP_READONLY или IPROP_READWRITE. 
  
## <a name="see-also"></a>См. также



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

