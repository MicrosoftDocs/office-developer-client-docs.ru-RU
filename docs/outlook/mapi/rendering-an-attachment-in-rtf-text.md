---
title: Отображение вложения в виде текста RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562976"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Отображение вложения в виде текста RTF

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Текст в формате RTF (RTF)-принять во внимание клиентов можно получить сведения положение отображения из текста сообщения RTF ищет следующие escape-последовательность в свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):
  
 `\objattph`
  
 **Чтобы найти сведения о визуализации в форматированный текст**
  
1. Вызов **IMessage::GetAttachmentTable** для доступа к таблице вложений сообщения. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Выполните построение ограничение свойство, которое ограничивает таблицу для строк, имеющих **PR_RENDERING_POSITION** не равно -1. Для получения дополнительных сведений см **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Вызов **IMAPITable::Restrict** для установки ограничений. Для получения дополнительных сведений см [IMAPITable::Restrict](imapitable-restrict.md).
    
4. Вызов **IMAPITable::SortTable** для сортировки вложения. Для получения дополнительных сведений см [IMAPITable::SortTable](imapitable-sorttable.md).
    
5. Вызов **IMAPITable::QueryRows** для получения соответствующих строк. Для получения дополнительных сведений см [IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Вызовите метод **IMAPIProp::OpenProperty** сообщений для получения **PR_RTF_COMPRESSED** с помощью интерфейса **IStream** . Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED**.
    
7. Проверка потока, ищите заполнитель визуализации, `\objattph`. Символ, следующий этот заполнитель — это место для следующего вложения в таблице сортировки.
    

