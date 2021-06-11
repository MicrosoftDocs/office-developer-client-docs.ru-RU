---
title: Открытие хранилища сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436029"
---
# <a name="opening-the-default-message-store"></a>Открытие хранилища сообщений по умолчанию

**Область применения**: Outlook 2013 | Outlook 2016 
  
В любом конкретном сеансе один магазин сообщений действует как хранилище сообщений по умолчанию. Хранилище сообщений по умолчанию имеет следующие характеристики:
  
- Свойство **PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)имеет свойство TRUE.
    
- Флаг STATUS_DEFAULT_STORE установлен в **свойстве PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
- MAPI автоматически создает подтрий IPM и корневые папки для результатов поиска, общих представлений и личных представлений при открытие магазина сообщений. Дополнительные сведения об этих папках см. в специальной папке [IPM Subtree](ipm-subtree.md) и [MAPI.](mapi-special-folders.md) 
    
Чтобы получить идентификатор записи для магазина сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы открыть таблицу хранения сообщений и применить соответствующее ограничение в вызове [в HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** возвращает набор строк с одной строкой, представляюной хранилище сообщений по умолчанию. Ограничение, которое вы передаете **в HrQueryAllRows,** может принимать одну из следующих форм: 
  
1. Ограничение **AND,** использующее **структуру SAndRestriction** для объединения: 
    
   - Существует ограничение, использующее **структуру SExistRestriction** для проверки наличия **свойства** PR_DEFAULT_STORE. 
    
   - Ограничение свойства, использующее [структуру SPropertyRestriction](spropertyrestriction.md) для проверки значения TRUE в **свойстве** PR_DEFAULT_STORE. 
    
2. Ограничение bitmask, использующее структуру [SBitMaskRestriction](sbitmaskrestriction.md) для применения STATUS_DEFAULT_STORE в качестве маски PR_RESOURCE_FLAGS **свойства.** 
    
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

