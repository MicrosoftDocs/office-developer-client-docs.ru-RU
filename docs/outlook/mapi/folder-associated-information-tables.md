---
title: Folder-Associated информационные таблицы
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
# <a name="folder-associated-information-tables"></a>Folder-Associated информационные таблицы

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI определяет флаг MAPI_ASSOCIATED для различных компонентов MAPI, которые необходимо использовать при работе с связанными таблицами информации. Каждая папка в хранилище сообщений должна иметь связанную таблицу содержимого вместе со стандартной таблицей содержимого. Клиентские приложения хранят специальные сообщения в связанной таблице содержимого папки для хранения форм и представлений. Фактически для поддержки форм и представлений поставщик магазина сообщений должен реализовать связанные таблицы контента.
  
Чтобы реализовать связанные таблицы контента, поставщик магазина должен выполнить следующие меры:
  
- Поддержка флага MAPI_ASSOCIATED в методе [IMAPIContainer::GetContentsTable,](imapicontainer-getcontentstable.md) чтобы клиентские приложения могли получать связанную таблицу содержимого папки вместо стандартной таблицы содержимого. 
    
- Поддержка флага MAPI_ASSOCIATED в методе [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md) чтобы клиентские приложения могли добавлять сообщения в связанную таблицу содержимого папки. 
    
- Установите MAPI_ACCESS_CREATE_ASSOCIATED в **свойстве PR_ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)на объектах папок.
    
- Поддержка флага DEL_ASSOCIATED в [методе IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md) 
    
- Установите MSGFLAG_ASSOCIATED в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)для сообщений в связанной таблице содержимого.
    
- Подвергайте и реагируйте на **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в папках.
    
- Сохранение **свойства PR_ASSOC_CONTENT_COUNT** [(PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)в папках.
    
В свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)нет бита, чтобы указать, поддерживает ли поставщик магазина сообщений связанные таблицы контента. Если поставщик магазина сообщений не поддерживает их, он должен возвращать MAPI_E_NO_SUPPORT, когда клиентские приложения звонят любым из вышеуказанных методов с MAPI_ASSOCIATED флагом.
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

