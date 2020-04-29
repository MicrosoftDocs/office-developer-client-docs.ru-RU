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
  
В каждом конкретном сеансе одно хранилище сообщений действует как хранилище сообщений по умолчанию. Хранилище сообщений по умолчанию имеет следующие характеристики:
  
- Для свойства **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) задано значение true.
    
- Флаг STATUS_DEFAULT_STORE задается в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI автоматически создает поддерево IPM и корневые папки для результатов поиска, общих представлений и персональных представлений при открытии хранилища сообщений. Дополнительные сведения об этих папках можно найти в разделе [IPM subtree](ipm-subtree.md) и [специальные папки MAPI](mapi-special-folders.md). 
    
Чтобы получить идентификатор записи для хранилища сообщений по умолчанию, необходимо вызвать [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) , чтобы открыть таблицу "хранилище сообщений" и применить соответствующее ограничение в вызове [хркуеряллровс](hrqueryallrows.md). **Хркуеряллровс** будет возвращать набор строк с одной строкой, представляющей хранилище сообщений по умолчанию. Ограничение, которое передается в **хркуеряллровс** , может принимать одну из следующих форм: 
  
1. Ограничение **, в котором** используется структура **сандрестриктион** для объединения: 
    
   - Ограничение EXISTS, использующее структуру **сексистрестриктион** для проверки существования свойства **PR_DEFAULT_STORE** . 
    
   - Ограничение свойства, использующее структуру [спропертирестриктион](spropertyrestriction.md) для проверки истинности значения свойства **PR_DEFAULT_STORE** . 
    
2. Ограничение битовой маски, использующее структуру [сбитмаскрестриктион](sbitmaskrestriction.md) для применения STATUS_DEFAULT_STORE в качестве маски к свойству **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

