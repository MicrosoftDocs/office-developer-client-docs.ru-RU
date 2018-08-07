---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809405"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к информации о хранилища сообщений и сообщений и папок.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объект хранилища сообщений  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |Клиентские приложения, диспетчер очереди MAPI и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMsgStore  <br/> |
|Тип указателя:  <br/> |LPMDB  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Уведомить](imsgstore-advise.md) <br/> |Регистрация для получения уведомлений о указанного события, которые влияют на хранилище сообщений.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **IMsgStore::Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Сравнение двух идентификаторы записей для определения, является ли они ссылаются на той же операции в банке сообщений.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшей доступа.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Устанавливает папки в качестве назначения для входящих сообщений класса определенного сообщения.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Получает к папке, где были установлены как место назначения для входящих сообщений из указанного класса сообщений или по умолчанию получают папки для хранения сообщений.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Предоставляет доступ к таблице папок получения таблицу, содержащую сведения обо всех получения папки для хранения сообщений.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Включение упорядоченного выхода хранилища сообщений.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Пытается удалить сообщения из очереди исходящих сообщений.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Предоставляет доступ к таблице исходящей очереди, таблицы, которая содержит сведения обо всех сообщений в очереди исходящих хранилища сообщений.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Блокирует или разблокирует сообщение.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Включает поставщика хранилища сообщений для обработки на отправленное сообщение.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |����������� ��������� ���������, ����� ���������.  <br/> |
   
|**Обязательные свойства**|**Уровень доступа**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
Для хранилищ сообщений электронной почты — это сообщение (IPM) выполнение следующих условий:
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)

