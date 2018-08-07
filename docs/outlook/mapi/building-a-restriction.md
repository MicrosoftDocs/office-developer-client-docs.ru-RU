---
title: Построение ограничение
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808122"
---
# <a name="building-a-restriction"></a>Построение ограничение

**Относится к**: Outlook 
  
Для построения ограничение, клиентское приложение создает иерархию структур ограничение одного или нескольких различных типов и передает указатель в иерархии, чтобы метод [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md) . Примеры кода в [Коде ограничение](sample-restriction-code.md) и приведенном ниже рисунке демонстрация реализации типичные ограничения структуры связанного ограничение различных типов. 

В этом примере пользователь клиентское приложение пытается найти все сообщения, содержащие слово «воллейбол» в строке темы и были отправлены Сью от Sam. Во-первых выделенный универсальная структура [SRestriction](srestriction.md) . Эта структура станет основой для других вызовов функции [MAPIAllocateMore](mapiallocatemore.md) для создания связанного [SRestriction](srestriction.md) и [SPropValue](spropvalue.md) структуры, которые можно освободить с помощью одного вызова [MAPIFreeBuffer](mapifreebuffer.md). Так как критерии для применения к набор сообщений состоит из трех частей, структура ограничение верхнего уровня является **и** ограничение. Член **cRes** структуры [SAndRestriction](sandrestriction.md) задано значение 3 для указания три ограничения для оценки и его элементом **lpRes** задано значение три члена-массива структур **SRestriction** . 
  
Чтобы найти сообщения, отправленные для определенного получателя, необходимое для поиска в таблице получателей для каждого сообщения, а не само сообщение. Ограничение вложенные объекты используется для выполнения поиска в таблице получателей. Таким образом первый элемент массива указывает на структуру [SSubRestriction](ssubrestriction.md) с его **ulSubObject** набор элементов в **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Нажмите чтобы указать, что следует искать в таблице получателей, используется ограничение содержимого. 
  
Второй и третий элементы массива, более простые. Оба пункты структуры ограничение содержимого, одно для поиска сообщения, для которых значение «Sam», а другое свойство **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), который имеет свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), задайте значение» воллейбол.»
  
**Внедрение ограничения**
  
![Реализация ограничений] (media/amapi_61.gif "Реализация ограничений")
  
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

