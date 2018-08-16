---
title: Проверка и инициализация хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812601"
---
# <a name="validating-and-initializing-a-message-store"></a>Проверка и инициализация хранилища сообщений

  
  
**Относится к**: Outlook 
  
При открытии хранилища сообщений через метод [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) без установки флага MDB_NO_MAIL MAPI создается несколько папок и присваивает им имена по умолчанию и роли. MAPI несет ответственность за создание этих папок, чтобы избежать несовместимости, неизменно может возникать, если были ответственность за создание клиентов или поставщиков хранилища сообщений. 
  
Иногда бывает необходимо убедиться, что были созданы соответствующие папки и что они действительны. Функция [HrValidateIPMSubtree](hrvalidateipmsubtree.md) доступна для этой цели. При проверке хранилище сообщений по умолчанию, передайте флаг MAPI_FULL_IPM_TREE. Расширенный группы папок будет создан хранилище сообщений по умолчанию. Когда **HrValidateIPMSubtree** Получает флаг MAPI_FULL_IPM_TREE, проверяет наличие следующих папках: 
  
- Корневой папки для поддерева IPM
    
- Папка "Удаленные" в корневой папке IPM
    
- Папка "Входящие" в корневой папке IPM
    
- Исходящие папки в корневой папке IPM
    
- Папка «Отправленные» в корневой папке IPM
    
- Представления папок в корневой папке хранилища сообщений
    
- Общие представления в корневую папку хранилища сообщений
    
- Папки поиска в корневую папку хранилища сообщений
    
Если хранилище сообщений не по умолчанию, можно задать или не задан флаг MAPI_FULL_IPM_TREE. Если этот флаг не задан, **HrValidateIPMSubtree** проверяет наличие только корневой папки для поддерева, папки «Удаленные», корневой папки для сообщения хранилища и результатов поиска. 
  
Для инициализации хранилища сообщений, хранят следующие свойства в памяти, чтобы они были легко доступны.
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Эти свойства — это битовой маски, описаны функции хранилища сообщений. **PR_VALID_FOLDER_MASK** имеет одно битовое значение для каждой отдельной папки, который существует в хранилище сообщений и имеет идентификатор назначенный запись, который является допустимым. Дополнительные сведения о доступе к этим папкам и их идентификаторы записей можно [Открытие папки хранения сообщений](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** имеет одно битовое значение для каждой функции, поддерживаемые в хранилище сообщений. К примеру Если хранилища сообщений поддерживает уведомления и форматированный текст, его **PR_STORE_SUPPORT_MASK** будут иметь набор битов STORE_NOTIFY_OK и STORE_RTF_OK. 
  
Другие свойства, которые должны сохраняться локально включают идентификаторы записей для папки, в которых описываются свойства **PR_VALID_FOLDER_MASK** как допустимый. Каждый из этих папок, за исключением папке "Входящие" имеет свойство идентификатор записи связанных с ним. Например идентификатор записи для папки "Исходящие" — это его свойство **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Так как эти папки все папках, которые будут открывать часто, рекомендуется иметь быстрый доступ к идентификаторам запись.
  
