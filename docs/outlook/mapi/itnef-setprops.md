---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 81f9388b67d3194fe1442091b9f4f75a7671cb6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579650"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает значение одного или нескольких свойств для инкапсулированное сообщение или вложение без изменения исходного сообщения или вложения. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как задать значения свойств. Можно задать следующий флаг:
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из сообщения или вложения, указанного с помощью параметра _ulElemID_ . 
    
 _ulElemID_
  
> [in] Свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения, которое содержит число, однозначно идентифицирует вложения в сообщение его родительского.
    
 _cValues_
  
> [in] Количество значений свойств в структуре [SPropValue](spropvalue.md) указывает параметр _lpProps_ . 
    
 _lpProps_
  
> [in] Указатель на структуру **SPropValue** , который содержит значения свойств свойства, которые нужно установить. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::SetProps** для настройки свойств для включения в инкапсуляция вложения или сообщения без изменения исходного сообщения или вложения. Все свойства, заданные с этим звонком переопределить существующие свойства в инкапсулированное сообщение. 
  
 **SetProps** поддерживается только для объектов TNEF, которые открываются с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) . С помощью этого вызова можно задать любое количество свойств. 
  
> [!NOTE]
> Без фактического кодировка TNEF для **SetProps** происходит до того времени, после вызова метода [ITnef::Finish](itnef-finish.md) . Данная функциональная возможность означает, что был передан в **SetProps** указатели должны оставаться действительно до, после **завершения** вызова. На этом этапе всех объектов и данных, передаваемых в **SetProps** вызовы можно выпущен или освобождении. 
  
## <a name="see-also"></a>См. также



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

