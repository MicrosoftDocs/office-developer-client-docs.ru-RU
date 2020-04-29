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
  
Предоставляет доступ к сведениям о хранилище сообщений, а также к сообщениям и папкам.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объект хранилища сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, диспетчер очереди MAPI и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMsgStore  <br/> |
|Тип указателя:  <br/> |лпмдб  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Рекомендуем](imsgstore-advise.md) <br/> |Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода **IMsgStore:: Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на одну и ту же запись в хранилище сообщений.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Открывает папку или сообщение и возвращает указатель интерфейса для получения дальнейших прав.  <br/> |
|[сетрецеивефолдер](imsgstore-setreceivefolder.md) <br/> |Устанавливает папку в качестве назначения для входящих сообщений определенного класса сообщений.  <br/> |
|[жетрецеивефолдер](imsgstore-getreceivefolder.md) <br/> |Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранилища сообщений.  <br/> |
|[жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) <br/> |Предоставляет доступ к таблице получения папки, в которой содержатся сведения обо всех папках получения для хранилища сообщений.  <br/> |
|[сторелогофф](imsgstore-storelogoff.md) <br/> |Позволяет выполнять упорядоченный выход из хранилища сообщений.  <br/> |
|[абортсубмит](imsgstore-abortsubmit.md) <br/> |Пытается удалить сообщение из исходящей очереди.  <br/> |
|[жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md) <br/> |Предоставляет доступ к таблице исходящей очереди, таблице, содержащей сведения обо всех сообщениях в исходящей очереди хранилища сообщений.  <br/> |
|[сетлоккстате](imsgstore-setlockstate.md) <br/> |Блокировка или разблокировка сообщения.  <br/> |
|[финишедмсг](imsgstore-finishedmsg.md) <br/> |Позволяет поставщику хранилища сообщений выполнять обработку отправленного сообщения.  <br/> |
|[нотифиневмаил](imsgstore-notifynewmail.md) <br/> |����������� ��������� ���������, ����� ���������.  <br/> |
   
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
   
Для хранилищ сообщений взаимосвязанных сообщений (IPM) используются следующие свойства:
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)

