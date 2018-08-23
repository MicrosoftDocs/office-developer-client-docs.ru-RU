---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590801"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Выполняет операции на сообщения и вложенных папок в папке.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты папок  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFolder  <br/> |
|Тип указателя:  <br/> |LPMAPIFOLDER  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Копирование или перемещение одно или несколько сообщений.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Удаляет одно или несколько сообщений.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Создает папку.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Копирование или перемещение вложенной папке.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Удаляет вложенной папке.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Задает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) из одного или нескольких сообщений, папок и управляет Отправка чтения отчеты.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Получение сведений о состоянии, связанные с сообщение в определенной папке.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Задание состояния, связанный с сообщением.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Задает порядок сортировки по умолчанию для папки содержимое таблицы.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Удаляет все сообщения и вложенные папки из папки без удаления самой папке.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

