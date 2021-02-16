---
title: Коды ошибок (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 390df5ce-e730-470d-b6e9-0de4a3e904f8
description: В этом разделе перечислены коды ошибок в объектной модели OneNote 2013.
ms.openlocfilehash: 83f8ad3d686693c82db1e57b8e37fa21ad140ab9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409428"
---
# <a name="error-codes-onenote"></a>Коды ошибок (OneNote)

В этом разделе перечислены коды ошибок в объектной модели OneNote 2013.
  
|**HResult**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|hrMalformedXML  <br/> |0x80042000  <br/> |XML не сформирован.  <br/> |
|hrInvalidXML  <br/> |0x80042001  <br/> |Недопустимый XML-xml.  <br/> |
|hrCreatingSection  <br/> |0x80042002  <br/> |Не удалось создать раздел.  <br/> |
|hrOpeningSection  <br/> |0x80042003  <br/> |Не удалось открыть раздел.  <br/> |
|hrSectionDoesNotExist  <br/> |0x80042004  <br/> |Раздел не существует.  <br/> |
|hrPageDoesNotExist  <br/> |0x80042005  <br/> |Страница не существует.  <br/> |
|hrFileDoesNotExist  <br/> |0x80042006  <br/> |Файл не существует.  <br/> |
|hrInsertingImage  <br/> |0x80042007  <br/> |Не удалось вставить изображение.  <br/> |
|hrInsertingInk  <br/> |0x80042008  <br/> |Не удалось вставить ink.  <br/> |
|hrInsertingHtml  <br/> |0x80042009  <br/> |Не удалось вставить HTML-код.  <br/> |
|hrNavigatingToPage  <br/> |0x8004200a  <br/> |Не удалось открыть страницу.  <br/> |
|hrSectionReadOnly  <br/> |0x8004200b  <br/> |Раздел находится только для чтения.  <br/> |
|hrPageReadOnly  <br/> |0x8004200c  <br/> |Страница находится только для чтения.  <br/> |
|hrInsertingOutlineText  <br/> |0x8004200d  <br/> |Не удалось вставить текст в структуру.  <br/> |
|hrPageObjectDoesNotExist  <br/> |0x8004200e  <br/> |Объект страницы не существует.  <br/> |
|hrBinaryObjectDoesNotExist  <br/> |0x8004200f  <br/> |Двоичный объект не существует.  <br/> |
|hrLastModifiedDateDidNotMatch  <br/> |0x80042010  <br/> |Дата последнего изменения не совпадает.  <br/> |
|hrGroupDoesNotExist  <br/> |0x80042011  <br/> |Группа разделов не существует.  <br/> |
|hrPageDoesNotExistInGroup  <br/> |0x80042012  <br/> |Страница не существует в группе разделов.  <br/> |
|hrNoActiveSelection  <br/> |0x80042013  <br/> |Активный выбор не существует.  <br/> |
|hrObjectDoesNotExist  <br/> |0x80042014  <br/> |Объект не существует.  <br/> |
|hrNotebookDoesNotExist  <br/> |0x80042015  <br/> |Записная книжка не существует.  <br/> |
|hrInsertingFile  <br/> |0x80042016  <br/> |Не удалось вставить файл.  <br/> |
|hrInvalidName  <br/> |0x80042017  <br/> |Недопустимое имя.  <br/> |
|hrFolderDoesNotExist  <br/> |0x80042018  <br/> |Папка (группа разделов) не существует.  <br/> |
|hrInvalidQuery  <br/> |0x80042019  <br/> |Недопустимый запрос.  <br/> |
|hrFileAlreadyExists  <br/> |0x8004201a  <br/> |Файл уже существует.  <br/> |
|hrSectionEncryptedAndLocked  <br/> |0x8004201b  <br/> |Раздел зашифрован и заблокирован.  <br/> |
|hrDisabledByPolicy  <br/> |0x8004201c  <br/> |Действие отключено политикой.  <br/> |
   
||||
|:-----|:-----|:-----|
|hrNotYetSynchronized  <br/> |0x8004201d  <br/> |В OneNote еще не синхронизировано содержимое.  <br/> |
|hrLegacySection  <br/> |0x8004201E  <br/> |Этот раздел находится в OneNote 2007 или более ранней.  <br/> |
|hrMergeFailed  <br/> |0x8004201F  <br/> |Сбой операции объединения.  <br/> |
|hrInvalidXMLSchema  <br/> |0x80042020  <br/> |Схема XML недействительна.  <br/> |
|hrFutureContentLoss  <br/> |0x80042022  <br/> |Произошла потеря содержимого (из будущих версий OneNote).  <br/> |
|hrTimeOut  <br/> |0x80042023  <br/> |Время действия было иным.  <br/> |
|hrRecordingInProgress  <br/> |0x80042024  <br/> |Аудиозапись идет.  <br/> |
|hrUnknownLinkedNoteState  <br/> |0x80042025  <br/> |Состояние связанной заметки неизвестно.  <br/> |
|hrNoShortNameForLinkedNote  <br/> |0x80042026  <br/> |Для связанной заметки нет короткого имени.  <br/> |
|hrNoFriendlyNameForLinkedNote  <br/> |0x80042027  <br/> |Для связанной заметки нет удобного имени.  <br/> |
|hrInvalidLinkedNoteUri  <br/> |0x80042028  <br/> |Недопустимый URI связанного заметки.  <br/> |
|hrInvalidLinkedNoteThumbnail  <br/> |0x80042029  <br/> |Недопустимый эскиз связанного заметки.  <br/> |
|hrImportLNTThumbnailFailed  <br/> |0x8004202A  <br/> |Не удалось импортировать связанный эскиз заметки.  <br/> |
|hrUnreadDisabledForNotebook  <br/> |0x8004202B  <br/> |Непрочитанные выделения отключены для записной книжки.  <br/> |
|hrInvalidSelection  <br/> |0x8004202C  <br/> |Выбор недействителен.  <br/> |
|hrConvertFailed  <br/> |0x8004202D  <br/> |Сбой преобразования.  <br/> |
|hrRecycleBinEditFailed  <br/> |0x8004202E  <br/> |Сбой редактирования в корзине.  <br/> |
   
Ниже перечислены новые коды ошибок для OneNote 2013.
  
|**HResult**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|hrIMConversationTypeInvalid  <br/> |0x8004202F  <br/> |Возвращается **UpdatePageContent,** если свойство узла страницы **IMConversationType** имеет значение, не от 0,1,2 или 3  <br/> |
|hrAppInModalUI  <br/> |0x80042030  <br/> |Модальные диалоговое окно блокирует приложение.  <br/> |
   
## <a name="see-also"></a>См. также

- [Справочник разработчика для OneNote](onenote-developer-reference.md)

