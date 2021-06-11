---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437653"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Кодирует представление таблицы получателей сообщения в потоке Transport-Neutral формата Инкапсуляции (TNEF) для сообщения.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpRecipientTable_
  
> [in] Указатель на таблицу получателей, для которой кодируются представления. Параметр  _lpRecipientTable может_ быть NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::EncodeRecips** для выполнения кодирования TNEF для определенного представления таблицы получателей. Кодификат TNEF полезен, например, если поставщику или шлюзу требуется определенный набор столбцов, порядок сортировки или ограничение для таблицы получателей. 
  
Поставщик или шлюз передает представление таблицы, кодированное в _параметре lpRecipientTable._ Реализация TNEF кодирует таблицу получателей с заданным представлением, используя заданный набор столбцов, порядок сортировки, ограничение и положение. Если поставщик или шлюз передает NULL в  _lpRecipientTable,_ TNEF получает таблицу получателей из зашифрованного сообщения с помощью метода [IMessage::GetRecipientTable](imessage-getrecipienttable.md) и обрабатывает каждую строку таблицы в поток TNEF с помощью текущих параметров таблицы. 
  
Вызов **EncodeRecips** с NULL в _lpRecipientTable_ таким образом кодирует всех получателей сообщений и эквивалентен вызову метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в его параметре _ulFlags_ и **свойством PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в параметре _lpPropList._ 
  
Обратите внимание, что редко необходимо вызывать **EncodeRecips,** если не требуется кодировать определенное представление таблицы получателей. В иностранных системах обмена сообщениями почти всегда есть возможности для обработки списков получателей, которые достаточно мощны для обработки общих потребностей списков получателей; поэтому эти системы почти никогда не требуют TNEF для этой цели. 
  
## <a name="see-also"></a>См. также



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

