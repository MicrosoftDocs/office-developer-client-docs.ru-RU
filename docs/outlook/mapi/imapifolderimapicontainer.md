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
  
Выполняет операции над сообщениями и вложенными папками в папке.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты папок  <br/> |
|Реализовано в:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапифолдер  <br/> |
|Тип указателя:  <br/> |ЛПМАПИФОЛДЕР  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[Копимессажес](imapifolder-copymessages.md) <br/> |Копирует или перемещает одно или несколько сообщений.  <br/> |
|[Делетемессажес](imapifolder-deletemessages.md) <br/> |Удаляет одно или несколько сообщений.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Создает новую вложенную папку.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Копирует или перемещает вложенную папку.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Удаляет вложенную папку.  <br/> |
|[Сетреадфлагс](imapifolder-setreadflags.md) <br/> |Задает или очищает флаг МСГФЛАГ_РЕАД в свойстве **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) одного или нескольких сообщений папки и управляет отправкой отчетов о прочтении.  <br/> |
|[Жетмессажестатус](imapifolder-getmessagestatus.md) <br/> |Получает состояние, связанное с сообщением в определенной папке.  <br/> |
|[Сетмессажестатус](imapifolder-setmessagestatus.md) <br/> |Задает состояние, связанное с сообщением.  <br/> |
|[Савеконтентссорт](imapifolder-savecontentssort.md) <br/> |Задает порядок сортировки по умолчанию для таблицы содержимого папки.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Удаляет все сообщения и вложенные папки из папки без удаления самой папки.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**Пр_дисплай_наме** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_фолдер_типе** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

