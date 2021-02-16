---
title: Создание ограничения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422512"
---
# <a name="building-a-restriction"></a>Создание ограничения

**Относится к**: Outlook 2013 | Outlook 2016 
  
Для создания ограничения клиентские приложения создают иерархию одной или более структур ограничений различных типов и передает указатель на иерархию методу [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow.](imapitable-findrow.md) На иллюстрации к примеру [](sample-restriction-code.md) кода в примере кода ограничений показано, как типичное ограничение реализуется со связанными структурами ограничений разных типов. 

В этом примере пользователь клиентского приложения пытается найти все сообщения, которые содержат слово "замещение" в строке темы и были отправлены Ерменой от Sam. Во-первых, выделяется общая [структура SRestriction.](srestriction.md) Эта структура становится основой для других вызовов функции [MAPIAllocateMore](mapiallocatemore.md) для создания связанных [структур SRestriction](srestriction.md) и [SPropValue,](spropvalue.md) которые можно освободить одним вызовом [MAPIFreeBuffer](mapifreebuffer.md). Поскольку критерии, которые необходимо применить к набору сообщений, относятся к трем частям, структура ограничений верхнего уровня является **ограничением AND.** Для члена **CRes** структуры [SAndRestriction](sandrestriction.md) установлено 3, чтобы указать три ограничения для оценки, а для его члена **lpRes** установлено три члена массива структур **SRestriction.** 
  
Для поиска сообщений, отправленных определенному получателю, необходимо найти в таблице получателей каждое сообщение, а не само сообщение. Для поиска таблицы получателей используется ограничение подобектов. Таким образом, первый член массива указывает на структуру [SSubRestriction,](ssubrestriction.md) для ее члена **ulSubObject** установлено PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md) Затем, чтобы указать, что искать в таблице получателей, используется ограничение содержимого. 
  
Второй и третий члены массива являются более простыми. Оба они указывают на структуры ограничений содержимого, один для поиска сообщений, для свойства **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), для другого, для свойства **PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)задаваемого "ветвь".
  
**Внедрение ограничения**
  
![Реализация ограничения реализации](media/amapi_61.gif "ограничений")
  
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

