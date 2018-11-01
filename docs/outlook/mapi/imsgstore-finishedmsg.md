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
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589954"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает поставщика хранилища сообщений для обработки на отправленное сообщение. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи сообщения для обработки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Обработка в сообщении прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранения сообщения не поддерживает обработки отправленных сообщений. Это значение ошибка возвращается в том случае, если вызывающий объект не является диспетчер очереди MAPI.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::FinishedMsg** выполняет обработку отправленных сообщений. В этом обработки может включать в себя удаление сообщений, перемещения в другую папку или оба действия. Тип обработки зависит от того, является ли значение свойства **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) и **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

В реализации **FinishedMsg**разблокировки сообщения, определяемую средством _lpEntryID_ и выполнить необходимые операции. Сообщение целевой всегда будут удалены; Диспетчер очереди MAPI никогда не передает идентификатор записи для разблокированными сообщения **FinishedMsg**.
  
Существует возможность, что ни имеет значение **PR_DELETE_AFTER_SUBMIT** или **PR_SENTMAIL_ENTRYID** , как задать или задать одно или другое. В следующей таблице описываются действия необходимо выполнить на основе параметров: 
  
|||
|:-----|:-----|
|Если ни один из свойство имеет значение:  <br/> |Оставьте сообщение в папку, из которого был отправлен (обычно исходящие).  <br/> |
|Если заданы оба свойства:  <br/> |Перемещение сообщения в указанной папки, если это необходимо и затем удалите его.  <br/> |
|Если значение PR_SENTMAIL_ENTRYID:  <br/> |Перемещение сообщения в указанной папке.  <br/> |
|Если значение PR_DELETE_AFTER_SUBMIT:  <br/> |Удалите сообщение.  <br/> |
   
После выполнения действие соответствующие вызовите метод [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>См. также



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

