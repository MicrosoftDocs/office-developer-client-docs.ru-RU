---
title: имсгсторефинишедмсг
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику хранилища сообщений выполнять обработку отправленного сообщения. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _лпентрид_
  
> возврата Указатель на идентификатор записи обрабатываемого сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Обработка отправленного сообщения выполнена успешно.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранилища сообщений не поддерживает отправную обработку сообщений. Это значение ошибки возвращается, если вызывающий абонент не является диспетчером MAPI.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore:: финишедмсг** выполняет обработку отправленного сообщения. Эта обработка может привести к удалению сообщения, перемещению его в другую папку или обоим действиям. Тип обработки зависит от того, заданы ли свойства **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) и **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

В реализации **финишедмсг**Разблокируйте сообщение, определяемое _лпентрид_ , и выполните соответствующую обработку. Конечное сообщение всегда будет заблокировано; Диспетчер очереди MAPI никогда не передает идентификатор записи для незаблокированного сообщения в **финишедмсг**.
  
Возможно, не заданы ни **PR_DELETE_AFTER_SUBMIT** , ни **PR_SENTMAIL_ENTRYID** , заданы оба параметра либо заданы один или другой. В следующей таблице описаны действия, которые необходимо выполнить в соответствии с параметрами: 
  
|||
|:-----|:-----|
|Если не задано ни одно свойство:  <br/> |Оставьте сообщение в папке, из которой оно было отправлено (обычно это папка "исходящая").  <br/> |
|Если заданы оба свойства:  <br/> |При необходимости переместите сообщение в указанную папку, а затем удалите его.  <br/> |
|Если параметр PR_SENTMAIL_ENTRYID задан:  <br/> |Переместить сообщение в указанную папку.  <br/> |
|Если параметр PR_DELETE_AFTER_SUBMIT задан:  <br/> |Удаление сообщения.  <br/> |
   
Выполнив все необходимые действия, вызовите метод [имаписуппорт::D осентмаил](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>См. также



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

