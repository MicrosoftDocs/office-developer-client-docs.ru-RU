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
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424240"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет операции с сообщениями и вложенными папками в папке.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Выставим:  <br/> |Объекты папок  <br/> |
|Реализовано в:  <br/> |Поставщики store сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFolder  <br/> |
|Тип указателя:  <br/> |LPMAPIFOLDER  <br/> |
|Модель транзакций:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Копирует или перемещает одно или несколько сообщений.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Удаляет одно или несколько сообщений.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Создает новую ветвь.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Копирует или перемещает в подсайт.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Удаляет в подсайт.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)одного или более сообщений папки и управляет отправкой отчетов о прочтенных сообщениях.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Получает состояние, связанное с сообщением в определенной папке.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Задает состояние, связанное с сообщением.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Задает порядок сортировки по умолчанию для таблицы содержимого папки.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Удаляет все сообщения и вложенные папки из папки без удаления самой папки.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix)](pidtagdisplaynameprefix-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType)](pidtagfoldertype-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

