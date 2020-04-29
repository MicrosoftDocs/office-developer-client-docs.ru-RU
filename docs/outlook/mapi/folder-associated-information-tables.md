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
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426417"
---
# <a name="folder-associated-information-tables"></a>Таблицы сведений, связанных с папками

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов MAPI, которые используются при работе со связанными таблицами сведений. Каждая папка в хранилище сообщений должна содержать связанную таблицу с содержимым, а также ее стандартные таблицы контента. Клиентские приложения хранят специальные сообщения в таблице содержимого, связанной с папкой, для хранения форм и представлений. В действительности для поддержки форм и представлений поставщик хранилища сообщений должен реализовать связанные таблицы содержимого.
  
Для реализации связанных таблиц содержимого поставщик магазина должен выполнить следующие действия:
  
- Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) , чтобы клиентские приложения могли получить связанную с папкой таблицу содержимого, а не стандартные таблицы содержимого. 
    
- Поддерживает флаг MAPI_ASSOCIATED в методе [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) , чтобы клиентские приложения могли добавлять сообщения в таблицу с содержимым, связанным с папкой. 
    
- Установите бит MAPI_ACCESS_CREATE_ASSOCIATED в свойстве **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) объектов Folder.
    
- Поддерживает флаг DEL_ASSOCIATED в методе [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Установите бит MSGFLAG_ASSOCIATED в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) для сообщений в связанной таблице содержимого.
    
- Предоставление и ответ на свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в папках.
    
- Настройте свойство **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) для папок.
    
В свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) отсутствует бит, указывающий, поддерживает ли поставщик хранилища сообщений связанные таблицы содержимого. Если поставщик хранилища сообщений не поддерживает их, он должен возвратить MAPI_E_NO_SUPPORT, когда клиентские приложения вызывают любой из вышеупомянутых методов с флагом MAPI_ASSOCIATED.
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

