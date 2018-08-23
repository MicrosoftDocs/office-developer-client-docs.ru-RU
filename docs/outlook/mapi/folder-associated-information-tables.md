---
title: Таблицы сведений, связанных с папками
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9c9c75d0ae4b9fe060d6717dfa11ad418cbb715b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564649"
---
# <a name="folder-associated-information-tables"></a>Таблицы сведений, связанных с папками

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов интерфейса MAPI для использования при работе с таблицами связанные сведения. Каждой папке в хранилище сообщений должна быть таблица связанное содержимое вместе с его стандартных содержимое таблицы. Клиентские приложения хранятся специальные сообщения в таблице связанное содержимое папки для хранения формы и представления. На самом деле для поддержки формы и представления, поставщиком хранилища сообщений необходимо реализовать связанного содержимого таблицы.
  
Для реализации связанного содержимого таблицы, поставщиком хранилища необходимо выполните следующее:
  
- Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) , поэтому клиентские приложения можно получить таблицы связанного содержимого папки, а не в таблице стандартных содержимое. 
    
- Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) , поэтому клиентские приложения можно добавить сообщения к таблице связанное содержимое папки. 
    
- Установка бита MAPI_ACCESS_CREATE_ASSOCIATED в свойстве **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) на объектов папок.
    
- Поддерживает флаг DEL_ASSOCIATED в методе [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Задайте MSGFLAG_ASSOCIATED бит в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) для сообщений в таблице связанного содержимого.
    
- Предоставление доступа к и реагировать на свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) для папок.
    
- Ведение свойство **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) для папок.
    
Нет бит отсутствует в свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), указывающее, поддерживает ли поставщик хранилища сообщений связанного содержимого таблицы. Если поставщик хранилища сообщений не поддерживает их, она возвращает MAPI_E_NO_SUPPORT при вызове клиентских приложений, приведенных выше способов с флагом MAPI_ASSOCIATED.
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

