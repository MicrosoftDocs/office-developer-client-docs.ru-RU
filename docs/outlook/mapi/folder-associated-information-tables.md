---
title: Folder-Associated сведений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426417"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated сведений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов MAPI, которые будут применяться при работе со связанными информационными таблицами. Каждая папка в хранилище сообщений должна иметь связанную таблицу содержимого вместе со стандартной таблицей содержимого. Клиентские приложения хранят специальные сообщения в связанной с папкой таблице содержимого для хранения форм и представлений. Для поддержки форм и представлений поставщику содержимого необходимо реализовать связанные таблицы содержимого.
  
Для реализации связанных таблиц содержимого поставщик вашего магазина должен выполнить следующие меры.
  
- Поддержка флага MAPI_ASSOCIATED в методе [IMAPIContainer::GetContentsTable,](imapicontainer-getcontentstable.md) чтобы клиентские приложения могли получить связанную с папкой таблицу содержимого вместо стандартной таблицы содержимого. 
    
- Поддержка флага MAPI_ASSOCIATED в методе [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md) чтобы клиентские приложения могли добавлять сообщения в связанную с папкой таблицу содержимого. 
    
- Установите бит MAPI_ACCESS_CREATE_ASSOCIATED в свойстве **PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)для объектов папок.
    
- Поддержка флага DEL_ASSOCIATED в [методе IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md) 
    
- Задайте MSGFLAG_ASSOCIATED в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)для сообщений в связанной таблице содержимого.
    
- Предоставляете и реагируйте **на PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в папках.
    
- **Поддержив PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)в папках.
    
В свойстве PR_STORE_SUPPORT_MASK  [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)нет бита, чтобы указать, поддерживает ли поставщик связанного содержимого таблицы содержимого. Если поставщик вашего магазина сообщений не поддерживает их, он должен возвращать MAPI_E_NO_SUPPORT, когда клиентские приложения вызовят любой из вышеперечисленных методов с MAPI_ASSOCIATED флагом.
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

