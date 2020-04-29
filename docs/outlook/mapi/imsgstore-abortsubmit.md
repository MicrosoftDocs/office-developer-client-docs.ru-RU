---
title: имсгстореабортсубмит
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414384"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Пытается удалить сообщение из исходящей очереди.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _лпентрид_
  
> возврата Указатель на идентификатор элемента, который необходимо удалить из очереди исходящих сообщений. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно удалено из исходящей очереди.
    
MAPI_E_NOT_IN_QUEUE 
  
> Сообщение, определяемое _лпентрид_ , больше не находится в исходящей очереди хранилища сообщений, как правило, потому что оно уже отправлено. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Сообщение, определяемое _лпентрид_ , заблокировано диспетчером MAPI, и операция не может быть прервана. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore:: абортсубмит** пытается удалить отправленное сообщение из исходящей очереди хранилища сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После отправки сообщения прекращение отправки с помощью вызова **абортсубмит** является единственным действием, которое можно выполнить над сообщением. Не следует ожидать, что **абортсубмит** всегда будет успешным. В зависимости от того, как реализована базовая система обмена сообщениями, отменить отправку сообщения может быть невозможно. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Фолдердлг. cpp  <br/> |Кфолдердлг:: Онабортсубмит  <br/> |MFCMAPI использует метод **IMsgStore:: абортсубмит** , чтобы отменить отправку выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

