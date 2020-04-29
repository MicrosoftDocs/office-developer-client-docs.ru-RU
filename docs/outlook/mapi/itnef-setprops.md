---
title: итнефсетпропс
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
  
Задает значение одного или нескольких свойств для инкапсулированного сообщения или вложения, не изменяя исходное сообщение или вложение. 
  
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
  
> возврата Битовая маска флагов, определяющих, как устанавливаются значения свойств. Можно задать следующий флаг:
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из сообщения или вложения, заданного параметром _улелемид_ . 
    
 _улелемид_
  
> возврата Свойство **PR_ATTACH_NUM** вложения ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), которое содержит число, уникально идентифицирующее вложение в родительском сообщении.
    
 _квалуес_
  
> возврата Число значений свойств в структуре [спропвалуе](spropvalue.md) , на которую указывает параметр _лппропс_ . 
    
 _лппропс_
  
> возврата Указатель на структуру **спропвалуе** , которая содержит значения свойств свойств, которые необходимо задать. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод **итнеф:: SetProps** , чтобы задать свойства, включаемые в инкапсуляцию сообщения или вложения, не изменяя исходное сообщение или вложение. Все свойства, заданные с помощью этого вызова, переопределяют существующие свойства в инкапсулированном сообщении. 
  
 **SetProps** поддерживается только для объектов TNEF, открытых с флагом TNEF_ENCODE для функции [опентнефстреам](opentnefstream.md) или [опентнефстреамекс](opentnefstreamex.md) . С этим вызовом можно задать любое количество свойств. 
  
> [!NOTE]
> Фактическое кодирование TNEF для **SetProps** происходит до тех пор, пока не будет вызван метод [Итнеф:: Finish](itnef-finish.md) . Эта функция означает, что указатели, передаваемые в **SetProps** , должны быть действительными до выполнения вызова метода **Finish** . В этот момент все объекты и данные, переданные в вызовы **SetProps** , могут быть освобождены или освобождены. 
  
## <a name="see-also"></a>См. также



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

