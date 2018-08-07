---
title: Коды ошибок (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 390df5ce-e730-470d-b6e9-0de4a3e904f8
description: В этом разделе перечислены коды ошибок в объектной модели OneNote 2013.
ms.openlocfilehash: 58c4d5d96182c49a1bc447c44763b9aaef1734ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807649"
---
# <a name="error-codes-onenote"></a>Коды ошибок (OneNote)

В этом разделе перечислены коды ошибок в объектной модели OneNote 2013.
  
|**HResult**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|hrMalformedXML  <br/> |0x80042000  <br/> |XML-код не является правильным.  <br/> |
|hrInvalidXML  <br/> |0x80042001  <br/> |XML-код является недопустимым.  <br/> |
|hrCreatingSection  <br/> |0x80042002  <br/> |Не удалось создать раздел.  <br/> |
|hrOpeningSection  <br/> |0x80042003  <br/> |Не удается открыть раздел.  <br/> |
|hrSectionDoesNotExist  <br/> |0x80042004  <br/> |Раздел не существует.  <br/> |
|hrPageDoesNotExist  <br/> |0x80042005  <br/> |Страница не существует.  <br/> |
|hrFileDoesNotExist  <br/> |0x80042006  <br/> |Файл не существует.  <br/> |
|hrInsertingImage  <br/> |0x80042007  <br/> |Не удается вставить изображение.  <br/> |
|hrInsertingInk  <br/> |0x80042008  <br/> |Не удается вставить рукописный ввод.  <br/> |
|hrInsertingHtml  <br/> |0x80042009  <br/> |Не удается вставить HTML-код.  <br/> |
|hrNavigatingToPage  <br/> |0x8004200a  <br/> |Не удалось открыть страницу.  <br/> |
|hrSectionReadOnly  <br/> |0x8004200b  <br/> |Раздел предназначен только для чтения.  <br/> |
|hrPageReadOnly  <br/> |0x8004200c  <br/> |Страница доступна только для чтения.  <br/> |
|hrInsertingOutlineText  <br/> |0x8004200d  <br/> |Не удалось вставить текст структуры.  <br/> |
|hrPageObjectDoesNotExist  <br/> |0x8004200e  <br/> |Объект page не существует.  <br/> |
|hrBinaryObjectDoesNotExist  <br/> |0x8004200f  <br/> |Двоичный объект не существует.  <br/> |
|hrLastModifiedDateDidNotMatch  <br/> |0x80042010  <br/> |Дата последнего изменения не соответствует.  <br/> |
|hrGroupDoesNotExist  <br/> |0x80042011  <br/> |Группа раздел не существует.  <br/> |
|hrPageDoesNotExistInGroup  <br/> |0x80042012  <br/> |Страница не существует в группе раздела.  <br/> |
|hrNoActiveSelection  <br/> |0x80042013  <br/> |Не выделен active.  <br/> |
|hrObjectDoesNotExist  <br/> |0x80042014  <br/> |Объект не существует.  <br/> |
|hrNotebookDoesNotExist  <br/> |0x80042015  <br/> |Записная книжка не существует.  <br/> |
|hrInsertingFile  <br/> |0x80042016  <br/> |Не удается вставить файл.  <br/> |
|hrInvalidName  <br/> |0x80042017  <br/> |Недопустимое имя.  <br/> |
|hrFolderDoesNotExist  <br/> |0x80042018  <br/> |Папка (раздел группа) не существует.  <br/> |
|hrInvalidQuery  <br/> |0x80042019  <br/> |Недопустимый запрос.  <br/> |
|hrFileAlreadyExists  <br/> |0x8004201a  <br/> |Файл уже существует.  <br/> |
|hrSectionEncryptedAndLocked  <br/> |0x8004201b  <br/> |В разделе зашифрован и заблокирован.  <br/> |
|hrDisabledByPolicy  <br/> |0x8004201c  <br/> |Действие отключено политикой.  <br/> |
   
||||
|:-----|:-----|:-----|
|hrNotYetSynchronized  <br/> |0x8004201d  <br/> |OneNote еще не синхронизирован содержимого.  <br/> |
|hrLegacySection  <br/> |0x8004201E  <br/> |Раздел является OneNote 2007 или более ранних версий.  <br/> |
|hrMergeFailed  <br/> |0x8004201F  <br/> |Не удалось выполнить операцию объединения.  <br/> |
|hrInvalidXMLSchema  <br/> |0x80042020  <br/> |Схема XML является недопустимым.  <br/> |
|hrFutureContentLoss  <br/> |0x80042022  <br/> |Контента потеря (в будущих версиях OneNote).  <br/> |
|hrTimeOut  <br/> |0x80042023  <br/> |Действие, истекло.  <br/> |
|hrRecordingInProgress  <br/> |0x80042024  <br/> |Запись звука находится в стадии разработки.  <br/> |
|hrUnknownLinkedNoteState  <br/> |0x80042025  <br/> |Состояние связанных заметок неизвестно.  <br/> |
|hrNoShortNameForLinkedNote  <br/> |0x80042026  <br/> |Краткое имя не существует для связанных заметок.  <br/> |
|hrNoFriendlyNameForLinkedNote  <br/> |0x80042027  <br/> |Понятное имя не существует для связанных заметок.  <br/> |
|hrInvalidLinkedNoteUri  <br/> |0x80042028  <br/> |Связанные заметки URI является недопустимым.  <br/> |
|hrInvalidLinkedNoteThumbnail  <br/> |0x80042029  <br/> |Эскиз связанных заметок является недопустимым.  <br/> |
|hrImportLNTThumbnailFailed  <br/> |0x8004202A  <br/> |Сбой импорта связанных заметок эскиз.  <br/> |
|hrUnreadDisabledForNotebook  <br/> |0x8004202B  <br/> |Непрочитанные выделение отключена для записной книжки.  <br/> |
|hrInvalidSelection  <br/> |0x8004202C  <br/> |Выделение является недопустимым.  <br/> |
|hrConvertFailed  <br/> |0x8004202D  <br/> |Сбой преобразования.  <br/> |
|hrRecycleBinEditFailed  <br/> |0x8004202E  <br/> |Сбой при редактировании в корзине.  <br/> |
   
В следующем списке перечислены новые коды ошибок для OneNote 2013.
  
|**HResult**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|hrIMConversationTypeInvalid  <br/> |0x8004202F  <br/> |Возвращаемые **UpdatePageContent** , если свойство узла **IMConversationType** страница была значение, отличное от 0,1,2 или 3  <br/> |
|hrAppInModalUI  <br/> |0x80042030  <br/> |Модальное диалоговое окно блокирует приложение.  <br/> |
   
## <a name="see-also"></a>См. также

- [Справочник разработчика для OneNote](onenote-developer-reference.md)

