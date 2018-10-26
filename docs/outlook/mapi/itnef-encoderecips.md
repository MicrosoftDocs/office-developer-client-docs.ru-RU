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
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584570"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Кодирует представления для таблицы получателей сообщения в потоке данных Transport-Neutral Encapsulation формата TNEF в сообщении.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpRecipientTable_
  
> [in] Указатель на таблицу получателей, для которого кодируется в представлении. Параметр _lpRecipientTable_ может быть NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::EncodeRecips** для выполнения кодировка TNEF для определенного получателя таблицы представления. Кодировка TNEF функция особенно полезна, например, если поставщик или шлюз требует определенного столбца, порядок сортировки или ограничения для получателей таблицы. 
  
Поставщик или шлюз передает в табличном представлении кодируемые с помощью параметра _lpRecipientTable_ . Реализация TNEF кодирует получателей таблица с заданным представления, с помощью набора данным столбцом, порядок сортировки, ограничения и положение. Если поставщик или шлюз передает NULL _lpRecipientTable_, TNEF получает таблицы получателя из сообщения с помощью метода [IMessage::GetRecipientTable](imessage-getrecipienttable.md) кодирования, процессов и каждой строки в таблице в поток TNEF с помощью текущие параметры таблицы. 
  
Вызов **EncodeRecips** с NULL в _lpRecipientTable_ таким образом кодирует всех получателей сообщений и эквивалентен вызову метода [ITnef::AddProps](itnef-addprops.md) с флагом TNEF_PROP_INCLUDE в его параметр _ulFlags_ и **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) свойство в его параметра _lpPropList_ . 
  
Обратите внимание на то, что это редко необходимо для вызова **EncodeRecips** , если не требуется для кодирования представление определенного получателя в таблице. Внешние системы обмена сообщениями почти всегда иметь средства для обработки получателей списков, которые являются недостаточно для удовлетворения распространенных потребностей кодирования получателей списков; Таким образом эти системы почти никогда не требуют TNEF для этой цели. 
  
## <a name="see-also"></a>См. также



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

