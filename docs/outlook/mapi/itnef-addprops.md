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
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809603"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Относится к**: Outlook 
  
Позволяет вызова поставщика услуг или шлюза добавить свойства к инкапсуляция вложения или сообщения. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как включены или исключены из инкапсуляция свойства. Можно задать следующие флажки:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Кодирует только свойства с помощью параметра _lpPropList_ , являющихся частью вложения в сообщении. 
    
TNEF_PROP_CONTAINED 
  
> Кодирует только свойства из вложений, указанного с помощью параметра _ulElemID_ . Если параметр _lpvData_ не может быть NULL, запись данных, на который указывает в инкапсуляция вложений в файл, указанный в свойстве **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Кодирует только свойства из сообщения или вложения, указанного с помощью параметра _ulElemID_ . Если установлен этот флаг, значение в _lpvData_ должно быть указатель [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) . 
    
TNEF_PROP_EXCLUDE 
  
> Кодирует все свойства не указан в параметре _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Кодирует все свойства, указанные в _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Кодирует только те свойства, указанные в _lpPropList_ , которые входят в состав сообщения. 
    
 _ulElemID_
  
> [in] Свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения, которое содержит число, однозначно идентифицирует вложения в сообщение его родительского. Параметр _ulElemID_ используется при запросе специальная обработка для вложения. Параметр _ulElemID_ должен иметь значение 0, пока флаг TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpvData_
  
> [in] Указатель на данные вложения, используемые для замены данных вложения, указанное в _ulElemID_. Параметр _lpvData_ должен иметь значение NULL, если не задано в _ulFlags_TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF.
    
 _lpPropList_
  
> [in] Указатель на список свойств, включаемых в или исключить из инкапсуляция.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::AddProps** свойств списка, чтобы быть включены или исключены из обработки Transport-Neutral Encapsulation формата TNEF сообщение или вложение. С помощью последовательных вызовов, поставщик или шлюз можно указать список свойств для добавления и кодирования или исключить из кодирования. Поставщики и шлюзов можно также использовать **AddProps** для предоставления правильность сведений о специальная обработка вложений. 
  
 **AddProps** поддерживается только для объектов TNEF, которые открываются с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Обратите внимание на то, что не фактическая кодировка TNEF происходит для **AddProps** до вызова метода [ITnef::Finish](itnef-finish.md) . Данная функциональная возможность означает, что был передан в **AddProps** указатели должны оставаться действительно до, после **завершения** вызова. На этом этапе всех объектов и данных, переданными **AddProps** вызовы можно выпущен или освобождении. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |Mfcmapi (en) метод **ITnef::AddProps** используется для копирования свойств из сообщения в формате TNEF поток.  <br/> |
   
## <a name="see-also"></a>См. также



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

