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
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422329"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к сведениям о хранилище сообщений, а также к письмам и папок.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Выставим:  <br/> |Объект store сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики store сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, пул MAPI и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMsgStore  <br/> |
|Тип указателя:  <br/> |LPMDB  <br/> |
|Модель транзакций:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[Консультация](imsgstore-advise.md) <br/> |Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Отменяет отправку уведомлений, которые ранее были настроены с помощью вызова метода **IMsgStore::Advise.**  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Сравнивает два идентификатора записей, чтобы определить, ссылаются ли они на ту же запись в хранилище сообщений.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшего доступа.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Устанавливает папку в качестве места назначения для входящих сообщений определенного класса сообщений.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Получает папку, которая была установлена в качестве места назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранения сообщений.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Предоставляет доступ к таблице папок получения, таблице со сведениями обо всех папках получения для хранения сообщений.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Включает упорядоченный вход в хранилище сообщений.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Пытается удалить сообщение из исходя такой очереди.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Предоставляет доступ к таблице исходяющих очередей, которая содержит сведения обо всех сообщениях в исходя такой очереди.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Блокирует или разблокирует сообщение.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Позволяет поставщику хранилище сообщений выполнять обработку отправленного сообщения.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |����������� ��������� ���������, ����� ���������.  <br/> |
   
|**Обязательные свойства**|**Уровень доступа**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)  <br/> |Только для чтения  <br/> |
   
Для хранилищ сообщений между межличностным сообщением (IPM) имеются следующие свойства:
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)

