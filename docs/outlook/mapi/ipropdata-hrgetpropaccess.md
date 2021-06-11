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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает уровень и состояние доступа для одного или более свойств объекта.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Parameters

 _lppPropTagArray_
  
> [in, out] На входе массив тегов свойств, которые указывают свойства для получения уровней и состояния доступа; в противном случае указатель на NULL, который указывает, что **HrGetPropAccess** должен получать уровни доступа и состояние для всех свойств. На выходе массив тегов свойств, для которых были извлечены флаги доступа и состояния. Флаги хранятся в массиве, на который указывает параметр _lprgulAccess._ 
    
 _lprgulAccess_
  
> [вышел] Указатель на массив битмакс флага. Каждая битмаска указывает уровни доступа или состояние или оба свойства для каждого свойства, указанные в массиве, указанных параметром _lpPropTagArray._ Два массива позиционно в том, что первая битмаска, на которую  _указывает lprgulAccess,_ описывает первое свойство, на которое  _указывает lpPropTagArray,_ и так далее. Для каждого тега свойств можно установить следующие флаги: 
    
|**Флаг уровня доступа**|**Флаг состояния**|
|:-----|:-----|
|IPROP_READONLY, что указывает на невозможности изменения свойства.  <br/> |IPROP_CLEAN, что указывает на то, что свойство не было изменено.  <br/> |
|IPROP_READWRITE, что указывает на то, что свойство может быть изменено.  <br/> |IPROP_DIRTY, что указывает на изменение свойства.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно возвращены флаги уровня доступа и состояния свойств.
    
## <a name="remarks"></a>Примечания

Метод **IPropData::HrGetPropAccess** извлекает набор флагов, который указывает уровень доступа и состояние для одного или более свойств. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих.

Вы можете использовать **HrGetPropAccess** для следующих целей: 
  
- Чтобы определить, изменил или удалил свойство writable клиента.
    
- Чтобы предотвратить изменение или удаление свойства клиентом с помощью [методов IMAPIProp.](imapipropiunknown.md) 
    
Если одно из свойств в массиве тегов свойств, на которые указывает  _lppPropTagArray,_ удалено, **hrGetPropAccess** задает запись массива до 0 на выходе. Если вы установите  _lppPropTagArray_ в NULL и одно из свойств объекта будет удалено, удаленное свойство возвращается в массив. 
  
Если свойство было изменено, IPROP_DIRTY в соответствующей записи в массиве, на который указывает _lprgulAccess._ Ни IPROP_READONLY, ни IPROP_READWRITE не будут установлены. 
  
Если свойство не было изменено или удалено, будет IPROP_READONLY или IPROP_READWRITE флаг. 
  
## <a name="see-also"></a>См. также



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

