---
title: Открытие хранилище сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810048"
---
# <a name="opening-the-default-message-store"></a>Открытие хранилище сообщений по умолчанию

**Относится к**: Outlook 
  
В любой определенным сеансом единое хранилище сообщений действует как хранилище сообщений по умолчанию. Хранилище сообщений по умолчанию имеет следующие характеристики:
  
- Свойство **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) имеет значение TRUE.
    
- Флаг STATUS_DEFAULT_STORE установлен в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI автоматически создает поддерева IPM и корневые папки для результатов поиска, общие и личные представления при открытии хранилища сообщений. Дополнительные сведения об этих папок можно [Поддерева](ipm-subtree.md) IPM и [Специальные папки MAPI](mapi-special-folders.md). 
    
Чтобы получить идентификатор записи для хранилища сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) для открытия в таблице хранилища сообщений и применить соответствующее ограничение в вызове [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** возвращает строку набор с одной строкой, который представляет хранилище сообщений по умолчанию. Ограничение, которое передается **HrQueryAllRows** может принимать одно из следующих форм: 
  
1. **И** ограничение, которое использует структуру **SAndRestriction** для объединения: 
    
   - Существует ограничение, которое использует структуру **SExistRestriction** для проверки наличия свойство **PR_DEFAULT_STORE** . 
    
   - Ограничение свойство, которое использует структуру [SPropertyRestriction](spropertyrestriction.md) для проверки для значение TRUE в свойстве **PR_DEFAULT_STORE** . 
    
2. Ограничение Битовая маска, которое использует структуру [SBitMaskRestriction](sbitmaskrestriction.md) применения STATUS_DEFAULT_STORE как маска со свойством **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

