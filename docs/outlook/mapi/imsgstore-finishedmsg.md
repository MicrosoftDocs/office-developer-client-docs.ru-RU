---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427089"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику хранения сообщений выполнять обработку отправленного сообщения. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи обрабатываемого сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Обработка отправленного сообщения прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик магазина сообщений не поддерживает обработку отправленных сообщений. Это значение ошибки возвращается, если вызываемая не является шпалером MAPI.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::FinishedMsg** выполняет обработку отправленного сообщения. Эта обработка может включать удаление сообщения, перемещение его в другую папку или оба действия. Тип обработки зависит от **того,** заданы ли свойства [PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)и **PR_SENTMAIL_ENTRYID** [(PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

В реализации **FinishedMsg** разблокировать сообщение, идентифицированное  _lpEntryID,_ и выполнить соответствующую обработку. Целевое сообщение всегда будет заблокировано; spooler MAPI никогда не передает идентификатор записи для разблокированного сообщения **в FinishedMsg**.
  
Не исключено,  что PR_DELETE_AFTER_SUBMIT **или PR_SENTMAIL_ENTRYID** не за установлено, либо установлено одно или другое. В следующей таблице описывается действие, необходимое для параметров: 
  
|||
|:-----|:-----|
|Если не установлено ни одно свойство:  <br/> |Оставьте сообщение в папке, из которой оно было отправлено (как правило, в папке Outbox).  <br/> |
|Если за набором обоих свойств:  <br/> |При желании переместим сообщение в указанную папку и удалите его.  <br/> |
|Если PR_SENTMAIL_ENTRYID установлено:  <br/> |Перемещение сообщения в указанную папку.  <br/> |
|Если PR_DELETE_AFTER_SUBMIT установлено:  <br/> |Удаление сообщения.  <br/> |
   
После принятия необходимых действий позвоните в [метод IMAPISupport::D OSentMail.](imapisupport-dosentmail.md) 
  
## <a name="see-also"></a>См. также



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

