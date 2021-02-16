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
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430793"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает значение одного или более свойств инкапсулированного сообщения или вложения без изменения исходного сообщения или вложения. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет настройками значений свойств. Можно установить следующий флаг:
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из сообщения или вложения, указанные параметром _ulElemID._ 
    
 _ulElemID_
  
> [in] Свойство PR_ATTACH_NUM **вложения** ([PidTagAttachNumber),](pidtagattachnumber-canonical-property.md)которое содержит номер, однозначно определяя вложение в родительском сообщении.
    
 _cValues_
  
> [in] Количество значений свойств в [структуре SPropValue,](spropvalue.md) на которые указывает параметр _lpProps._ 
    
 _lpProps_
  
> [in] Указатель на **структуру SPropValue,** которая содержит значения свойств, которые необходимо установить. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики store сообщений и шлюзы вызывают метод **ITnef::SetProps,** чтобы настроить свойства для инкапсуляции сообщения или вложения без изменения исходного сообщения или вложения. Все свойства, заданные с помощью этого вызова, переопредят существующие свойства в инкапсулированных сообщениях. 
  
 **SetProps** поддерживается только для объектов TNEF, которые открываются с TNEF_ENCODE флагом для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md) С помощью этого вызова можно настроить любое количество свойств. 
  
> [!NOTE]
> Фактическая кодировка TNEF для **SetProps** не происходит до тех пор, пока не будет вызван метод [ITnef::Finish.](itnef-finish.md) Эта функция означает, что указатели, переданные **в SetProps,** должны оставаться действительными до завершения вызова.  На этом этапе все объекты и данные, переданные в **вызовы SetProps,** можно освободить или освободить. 
  
## <a name="see-also"></a>См. также



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

