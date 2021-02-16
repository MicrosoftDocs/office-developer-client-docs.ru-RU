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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику или шлюзу вызываемой службы добавлять свойства в инкапсуляцию сообщения или вложения. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как свойства включаются в инкапсуляцию или исключаются из нее. Можно установить следующие флаги:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Кодирует только свойства в параметре  _lpPropList,_ которые являются частью вложений в сообщении. 
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из вложения, указанного параметром _ulElemID._ Если параметр _lpvData_ не имеет NULL, указанные данные будут записаны в инкапсуляцию вложения в файл, указанный свойством **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName).](pidtagattachtransportname-canonical-property.md)
    
TNEF_PROP_CONTAINED_TNEF 
  
> Кодирует только свойства из сообщения или вложения, указанные параметром _ulElemID._ Если этот флаг установлен, значением _в lpvData_ должен быть указатель [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
TNEF_PROP_EXCLUDE 
  
> Кодирует все свойства, не указанные в параметре _lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Кодирует все свойства, указанные в _lpPropList._ 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Кодирует только те свойства, которые указаны в  _lpPropList,_ которые являются частью самого сообщения. 
    
 _ulElemID_
  
> [in] Свойство PR_ATTACH_NUM **вложения** ([PidTagAttachNumber),](pidtagattachnumber-canonical-property.md)которое содержит номер, однозначно определяя вложение в родительском сообщении. Параметр  _ulElemID_ используется при запросе специальной обработки вложения. Параметр _ulElemID_ должен быть 0, если TNEF_PROP_CONTAINED флаг TNEF_PROP_CONTAINED_TNEF в параметре _ulFlags._ 
    
 _lpvData_
  
> [in] Указатель на данные вложения, используемые для замены данных вложения, указанного в _ulElemID._ Параметр _lpvData должен_ иметь NULL, если TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF в _ulFlags._
    
 _lpPropList_
  
> [in] Указатель на список свойств, которые необходимо включить или исключить из инкапсуляции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики store сообщений и шлюзы звонят **методу ITnef::AddProps,** чтобы перечислить свойства, которые необходимо включить или исключить из обработки сообщения или вложения в формате Transport-Neutral Encapsulation Format (TNEF). С помощью последовательных вызовов поставщик или шлюз может указать список свойств для добавления и кодирования или исключения из кодирования. Поставщики и шлюзы также могут использовать **AddProps** для предоставления сведений о любых специальных вложениях обработки. 
  
 **AddProps** поддерживается только для объектов TNEF, которые открываются с TNEF_ENCODE флагом для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Обратите внимание, что для **AddProps** не происходит фактическое кодировка TNEF до тех пор, пока не будет вызван метод [ITnef::Finish.](itnef-finish.md) Эта функция означает, что указатели, переданные **в AddProps,** должны оставаться действительными до завершения вызова.  На этом этапе все объекты и данные, переданные с помощью вызовов **AddProps,** можно освободить или освободить. 
  
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

