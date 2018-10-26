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
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594364"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обрабатывает отдельные компоненты из сообщения одно за раз в поток Transport-Neutral Encapsulation формата TNEF ().
  
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

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, какой компонент будет завершено. Необходимо задать одно или другое следующих флагов:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Обработка будет завершено для объекта вложений; параметр _ulComponentID_ содержит свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения. 
    
TNEF_COMPONENT_MESSAGE 
  
> Обработка будет завершено для объекта message. 
    
 _ulComponentID_
  
> [in] 0 для указания обработки для сообщения или свойство **PR_ATTACH_NUM** вложения для обработки. Если в параметре _ulFlags_ флаг TNEF_COMPONENT_MESSAGE, _ulComponentID_ должен иметь значение 0. 
    
 _lpCustomPropList_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий тегов свойств, чтобы указать свойства, переданной в параметре _lpCustomProps_ . Должен быть однозначного соответствия между каждое значение свойства в _lpCustomProps_ и тег свойства с помощью параметра _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) , который содержит значения для свойств для кодирования. 
    
 _lpPropList_
  
> [in] Указатель на структуру **SPropTagArray** , содержащий теги свойства для свойства, которые нужно кодировать. 
    
 _lppProblems_
  
> [out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) . Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом. Если NULL передается в параметре _lppProblems_ , возвращается массив проблема не свойство. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::FinishComponent** для выполнения TNEF обработки для одного компонента, сообщения или вложения, как указано в параметре _ulFlags_ флаг. 
  
Для обработки компонент необходимо включить, вызывающий поставщика или шлюз передайте флаг TNEF_COMPONENT_ENCODING _ulFlags_ [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции, которая открыта объект для получения кодировки. 
  
Передача значений в параметры _lpCustomPropList_ и _lpCustomProps_ выполняет компонент кодирования параметру, который выполняется с помощью метода [ITnef::SetProps](itnef-setprops.md) . Передача значения с помощью параметра _lpPropList_ выполняет компонент кодировки эквивалент, который выполняется с помощью метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в _ulFlags_. Передача этих значений позволяет выполнять кодировки с помощью одного вызова, а не несколько вызовов.
  
Реализация TNEF отчетов проблем кодировки TNEF потока без остановки процесса **FinishComponent** . Структура **STnefProblemArray** , возвращаемых в _lppProblems_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать. Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему. Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **FinishComponent** не возвращает отчет о проблеме обработаны успешно. 
  
Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lppProblems_; в этом случае возвращается массив не проблемы.
  
Значение, возвращаемое в _lppProblems_ действителен только в том случае, если вызов возвращает значение S_OK. Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре [STnefProblemArray](stnefproblemarray.md) . При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено, и вызывающему поставщика или шлюз не использовать или Бесплатная загрузка структуры. Если ошибки не обнаружены на звонок, вызывающий поставщика или шлюз должен высвободить память для **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

