---
title: Отображение вложение в текст RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812119"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Отображение вложение в текст RTF

  
  
**Применимо к**: Outlook 
  
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
    

