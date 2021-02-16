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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обрабатывает отдельные компоненты из сообщения по одному в поток Transport-Neutral формата инкапсуляции (TNEF).
  
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

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, какой компонент будет завершен. Должен быть установлен один или несколько следующих флагов:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Обработка для объекта вложения будет завершена; Параметр  _ulComponentID_ **содержит** PR_ATTACH_NUM ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)вложения. 
    
TNEF_COMPONENT_MESSAGE 
  
> Обработка для объекта сообщения будет завершена. 
    
 _ulComponentID_
  
> [in] 0, чтобы указать обработку сообщения или PR_ATTACH_NUM вложения для обработки.  Если в TNEF_COMPONENT_MESSAGE  _ulFlags_ задан флаг,  _ulComponentID_ должен иметь 0. 
    
 _lpCustomPropList_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит теги свойств, которые определяют свойства, переданные в _параметре lpCustomProps._ Между каждым значением свойства в  _lpCustomProps_ и тегом свойства в параметре  _lpCustomPropList_ должно быть соответствие "один к одному". 
    
 _lpCustomProps_
  
> [in] Указатель на структуру [SPropValue,](spropvalue.md) которая содержит значения свойств для кодируемых свойств. 
    
 _lpPropList_
  
> [in] Указатель на структуру **SPropTagArray,** которая содержит теги свойств для кодируемых свойств. 
    
 _lppProblems_
  
> [out] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства ,если таковые имеются, не были закодированы должным образом. Если в параметре  _lppProblems_ передается NULL, массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики параметров хранения сообщений и шлюзы звонят **методу ITnef::FinishComponent** для выполнения обработки TNEF для одного компонента, сообщения или вложения, как указано флагом, установленным в параметре _ulFlags._ 
  
Чтобы включить обработку компонентов, поставщик вызовов или шлюз передают флаг TNEF_COMPONENT_ENCODING в  _ulFlags_ для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) которая открывает объект для получения кодив. 
  
Передача значений в _параметрах lpCustomPropList_ и _lpCustomProps_ выполняет коду компонента, эквивалентную коде, выполняемой методом [ITnef::SetProps.](itnef-setprops.md) Передача значения в _параметре lpPropList_ выполняет коду компонента, эквивалентную коде, выполняемой методом [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE, установленным в _ulFlags._ Передача этих значений позволяет выполнять кодилеты с помощью одного вызова, а не нескольких вызовов.
  
Реализация TNEF сообщает о проблемах кодиации потока TNEF без остановки процесса **FinishComponent.** Структура **STnefProblemArray,** возвращаемая  _в lppProblems,_ указывает, какие атрибуты TNEF или свойства MAPI (если таковые имеются) не удалось обработать. Значение, возвращаемого в члене **scode** одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз может работать при предположении, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме, были успешно обработаны. 
  
Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL в  _lppProblems;_ в этом случае массив проблем не возвращается.
  
Возвращаемая в  _lppProblems_ значение допустимо, только если вызов возвращает S_OK. Когда S_OK возвращается, поставщик или шлюз должен проверить значения, возвращенные в [структуре STnefProblemArray.](stnefproblemarray.md) Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик или шлюз вызовов не должны использовать или освободить структуру. Если ошибка при вызове не возникает, поставщик или шлюз вызовов должен освободить память **для STnefProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

