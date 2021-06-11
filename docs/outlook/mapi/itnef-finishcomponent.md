---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416442"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обрабатывает отдельные компоненты из сообщения по одному в поток Transport-Neutral формата Инкапсуляции (TNEF).
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, какой компонент будет завершен. Необходимо установить один или другой из следующих флагов:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Обработка будет завершена для объекта вложения; параметр _ulComponentID_ **содержит свойство PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) 
    
TNEF_COMPONENT_MESSAGE 
  
> Обработка будет завершена для объекта сообщения. 
    
 _ulComponentID_
  
> [в] 0, чтобы указать обработку сообщения или PR_ATTACH_NUM свойства вложения, которое будет обработано.  Если флаг TNEF_COMPONENT_MESSAGE установлен в параметре  _ulFlags,_  _ulComponentID_ должен быть 0. 
    
 _lpCustomPropList_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит теги свойств, определяя свойства, переданные в _параметре lpCustomProps._ Между каждым значением свойства  _в lpCustomProps_ и тегом свойства в  _параметре lpCustomPropList_ должна быть корреспонденция по одному. 
    
 _lpCustomProps_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) которая содержит значения свойств для кодируемых свойств. 
    
 _lpPropList_
  
> [in] Указатель на структуру **SPropTagArray,** которая содержит теги свойств для кодируемых свойств. 
    
 _lppProblems_
  
> [вышел] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства, если таковые имеются, были неправильно закодированы. Если NULL передается в  _параметре lppProblems,_ массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::FinishComponent** для выполнения обработки TNEF для одного компонента, сообщения или вложения, как указано в флаге, заданном в параметре _ulFlags._ 
  
Чтобы включить обработку компонентов, поставщик вызовов или шлюз передают флаг TNEF_COMPONENT_ENCODING  _в ulFlags_ для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) открывающей объект для получения кодиляции. 
  
Передача значений в _параметрах lpCustomPropList_ и _lpCustomProps_ выполняет кодинг компонентов, эквивалентный значениям, выполняемым методом [ITnef::SetProps.](itnef-setprops.md) Передача значения в  _параметре lpPropList_ выполняет кодинг компонентов, эквивалентный методу [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в  _ulFlags_. Передача этих значений позволяет выполнять кодиры одним вызовом, а не несколькими вызовами.
  
Реализация TNEF сообщает о проблемах кодации потока TNEF без остановки процесса **FinishComponent.** Структура **STnefProblemArray,** возвращаемая  _в lppProblems,_ указывает, какие атрибуты TNEF или свойства MAPI, если таковые имеются, не удалось обрабатывать. Значение, возвращаемого  в члене кода одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз могут работать с предположением, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме, были успешно обработаны. 
  
Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL  _в lppProblems;_ В этом случае массив проблем не возвращается.
  
Возвращаемая в  _lppProblems_ величина действительна только в том случае, если вызов возвращается S_OK. Когда S_OK возвращается, поставщик или шлюз должны проверить значения, возвращенные в [структуре STnefProblemArray.](stnefproblemarray.md) Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик вызовов или шлюз не должны использовать или освободить структуру. Если при вызове не возникает ошибки, поставщик вызовов или шлюз должен освободить память **для STnefProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

