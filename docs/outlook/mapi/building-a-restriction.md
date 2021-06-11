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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы создать ограничение, клиентский приложение создает иерархию одной или более структур ограничений различных типов и передает указатель иерархии [методу IMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow.](imapitable-findrow.md) На рисунке, который следует, и примере кода в [примере Кода](sample-restriction-code.md) ограничений показано, как обычное ограничение реализуется с связанными структурами ограничений разных типов. 

В этом примере пользователь клиентского приложения пытается найти все сообщения, содержащие слово "волейбол" в строке темы и отправленные Сью из Sam. Сначала выделяется общая [структура SRestriction.](srestriction.md) Эта структура становится основой для других вызовов функции [MAPIAllocateMore](mapiallocatemore.md) для создания связанных [структур SRestriction](srestriction.md) и [SPropValue,](spropvalue.md) которые можно освободить одним вызовом [в MAPIFreeBuffer](mapifreebuffer.md). Так как критерии, применимые к набору сообщений, в трех частях, структура ограничения верхнего уровня является **ограничением AND.** Для члена CRes структуры  [SAndRestriction](sandrestriction.md) установлено 3, чтобы указать три ограничения для оценки, а член **lpRes** — три набора структур **SRestriction.** 
  
Для поиска сообщений, отосланных конкретному получателю, необходимо искать таблицу получателей для каждого сообщения, а не само сообщение. Для выполнения поиска таблицы получателей используется ограничение subobject. Поэтому первый член массива указывает на структуру [SSubRestriction](ssubrestriction.md) с ее членом **ulSubObject** с набором PR_MESSAGE_RECIPIENTS [(PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md)  Затем, чтобы указать, что искать в таблице получателей, используется ограничение контента. 
  
Второй и третий члены массива являются более простыми. Они указывают на структуры ограничений **контента,** один из них — для поиска сообщений с свойством [PR_SENDER_NAME (PidTagSenderName),](pidtagsendername-canonical-property.md)задаваемого "Sam", а другой — с свойством **PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)с свойством "волейбол".
  
**Внедрение ограничения**
  
![Ограничение реализации](media/amapi_61.gif "Ограничения реализации")
  
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

