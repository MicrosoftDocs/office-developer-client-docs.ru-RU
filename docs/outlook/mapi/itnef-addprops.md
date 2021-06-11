---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348624"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику услуг вызова или шлюзу добавлять свойства в инкапсуляцию сообщения или вложения. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют, как свойства включены или исключены из инкапсуляции. Можно установить следующие флаги:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Кодирует только свойства в параметре  _lpPropList,_ которые являются частью вложений в сообщении. 
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из вложения, указанного параметром _ulElemID._ Если параметр _lpvData_ не является NULL, указанные данные вписаны в инкапсуляцию вложения в файл, указанный свойством [PR_ATTACH_TRANSPORT_NAME (PidTagAttachTransportName).](pidtagattachtransportname-canonical-property.md) 
    
TNEF_PROP_CONTAINED_TNEF 
  
> Кодирует только свойства из сообщения или вложения, указанные _параметром ulElemID._ Если задан этот флаг, значение _в lpvData_ должно быть [указателем IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
TNEF_PROP_EXCLUDE 
  
> Кодирует все свойства, не указанные в _параметре lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Кодирует все свойства, указанные в _lpPropList._ 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Кодирует только те свойства, указанные в  _lpPropList,_ которые являются частью самого сообщения. 
    
 _ulElemID_
  
> [in] Свойство PR_ATTACH_NUM  [(PidTagAttachNumber),](pidtagattachnumber-canonical-property.md)которое содержит номер, который однозначно определяет вложение в родительском сообщении. Параметр  _ulElemID_ используется при запросе специальной обработки для вложения. Параметр _ulElemID_ должен быть 0, если флаг TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF в параметре _ulFlags._ 
    
 _lpvData_
  
> [in] Указатель на данные вложения, используемые для замены данных вложения, указанных в _ulElemID._ Параметр  _lpvData должен_ быть NULL, если TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF в  _ulFlags_.
    
 _lpPropList_
  
> [in] Указатель на список свойств, которые необходимо включить или исключить из инкапсуляции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::AddProps,** чтобы перечислить свойства, которые будут включены или исключены из формата Transport-Neutral Инкапсуляции (TNEF) обработки сообщения или вложения. С помощью последовательных вызовов поставщик или шлюз может указать список свойств, которые необходимо добавить и кодировать или исключить из кодирования. Поставщики и шлюзы также могут использовать **AddProps** для предоставления сведений о любых специальных вложениях обработки. 
  
 **AddProps** поддерживается только для объектов TNEF, которые открываются с TNEF_ENCODE флагом для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Обратите внимание, что фактическое кодировать TNEF для **AddProps** не происходит до тех пор, пока не будет вызван метод [ITnef::Finish.](itnef-finish.md) Эта функция означает, что указатели, переданные **в AddProps,** должны оставаться действительными до завершения вызова.  На этом этапе все объекты и данные, переданные с помощью **вызовов AddProps,** могут быть освобождены или освобождены. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI использует метод **ITnef::AddProps** для копирования свойств из сообщения в поток TNEF.  <br/> |
   
## <a name="see-also"></a>См. также



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

