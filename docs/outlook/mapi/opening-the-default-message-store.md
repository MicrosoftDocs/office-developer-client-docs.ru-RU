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

**Относится к**: Outlook 2013 | Outlook 2016 
  
В любом конкретном сеансе одно хранилище сообщений действует как хранилище сообщений по умолчанию. Хранилище сообщений по умолчанию имеет следующие характеристики:
  
- Свойству **PR_DEFAULT_STORE** ([PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)задается true.
    
- Флаг STATUS_DEFAULT_STORE устанавливается в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
- MAPI автоматически создает поддерево IPM и корневые папки для результатов поиска, общих представлений и личных представлений при открытом хранилище сообщений. Дополнительные сведения об этих папках см. в поддеревье [IPM](ipm-subtree.md) и [специальных папках MAPI.](mapi-special-folders.md) 
    
Чтобы получить идентификатор записи для хранения сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы открыть таблицу хранения сообщений и применить соответствующее ограничение в вызове [HrQueryAllRows.](hrqueryallrows.md) **HrQueryAllRows** возвращает набор строк с одной строкой, которая представляет хранилище сообщений по умолчанию. Ограничение, которое вы передаете **в HrQueryAllRows,** может приниматься в одной из следующих форм: 
  
1. Ограничение **AND,** использующее **структуру SAndRestriction** для объединения: 
    
   - Существует ограничение, использующее **структуру SExistRestriction** для проверки наличия PR_DEFAULT_STORE **свойства.** 
    
   - Ограничение свойств, использующее [структуру SPropertyRestriction](spropertyrestriction.md) для проверки значения TRUE в PR_DEFAULT_STORE **свойства.** 
    
2. Ограничение битовых масок, использующее структуру [SBitMaskRestriction](sbitmaskrestriction.md) для применения  STATUS_DEFAULT_STORE к свойству PR_RESOURCE_FLAGS. 
    
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

