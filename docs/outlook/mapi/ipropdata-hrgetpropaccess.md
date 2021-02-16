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
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433439"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает уровень доступа и состояние для одного или более свойств объекта.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Параметры

 _lppPropTagArray_
  
> [in, out] При вводе массив тегов свойств, которые указывают свойства, для которых необходимо получить уровни доступа и состояние; в противном случае указатель на значение NULL указывает, что **HrGetPropAccess** должен получать уровни доступа и состояние для всех свойств. В выходных данных массив тегов свойств, для которых были извлечены флаги доступа и состояния. Флаги хранятся в массиве, на который указывает параметр _lprgulAccess._ 
    
 _lprgulAccess_
  
> [out] Указатель на массив битовых заметок. Каждая битоваяmask указывает уровни доступа, состояние или оба свойства для каждого из свойств, указанных в массиве, на который указывает параметр _lpPropTagArray._ Два массива являются позициональными в том, что первая битоваяmask, на которую указывает  _lprgulAccess,_ описывает первое свойство, на которое  _указывает lpPropTagArray,_ и так далее. Для каждого тега свойства можно установить следующие флаги: 
    
|**Флаг уровня доступа**|**Флаг состояния**|
|:-----|:-----|
|IPROP_READONLY, что означает, что свойство не может быть изменено.  <br/> |IPROP_CLEAN, что указывает на то, что свойство не было изменено.  <br/> |
|IPROP_READWRITE, что указывает на то, что свойство можно изменить.  <br/> |IPROP_DIRTY, что указывает на то, что свойство было изменено.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно возвращены флаги уровня доступа и состояния для свойств.
    
## <a name="remarks"></a>Примечания

Метод **IPropData::HrGetPropAccess** извлекает набор флагов, который указывает уровень доступа и состояние для одного или более свойств. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих.

**HrGetPropAccess можно** использовать для следующих целей: 
  
- Чтобы определить, изменил ли клиент или удалил свойство для нашего клиента.
    
- Чтобы запретить клиенту изменять или удалять свойство с помощью методов [IMAPIProp.](imapipropiunknown.md) 
    
Если одно из свойств в массиве тегов свойств, на которые указывает  _lppPropTagArray,_ удалено, **HrGetPropAccess** устанавливает для записи массива значение 0 при выходе. Если для  _lppPropTagArray_ установлено NULL и одно из свойств объекта удалено, удаленное свойство возвращается в массиве. 
  
Если свойство было изменено, его флаг IPROP_DIRTY в соответствующей записи в массиве, на который указывает _lprgulAccess._ Ни IPROP_READONLY, ни IPROP_READWRITE не будет установлено. 
  
Если свойство не было изменено или удалено, будет установлен только IPROP_READONLY или IPROP_READWRITE флаг. 
  
## <a name="see-also"></a>См. также



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

