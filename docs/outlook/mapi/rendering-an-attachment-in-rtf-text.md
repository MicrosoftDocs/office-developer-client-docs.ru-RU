---
title: Отрисовка вложения в тексте RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439795"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Отрисовка вложения в тексте RTF

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты с RTF могут получать сведения о положении отображения из текста сообщения RTF, насмотрев следующую escape-последовательность в свойстве **PR_RTF_COMPRESSED** сообщения [(PidTagRtfCompressed):](pidtagrtfcompressed-canonical-property.md)
  
 `\objattph`
  
 **Поиск сведений об отрисовки в форматном тексте**
  
1. Вызовите **IMessage::GetAttachmentTable,** чтобы получить доступ к таблице вложений сообщения. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Создайте ограничение свойств, ограничивающее таблицу строками, **PR_RENDERING_POSITION** не равными -1. Дополнительные сведения **см. в PR_RENDERING_POSITION** ([PidTagRenderingPosition).](pidtagrenderingposition-canonical-property.md)
    
3. Вызов **IMAPITable::Restrict** для применения ограничения. Дополнительные сведения см. в [подразделе IMAPITable::Restrict.](imapitable-restrict.md)
    
4. Вызовите **IMAPITable::SortTable** для сортировки вложений. Дополнительные сведения см. в [подразделе IMAPITable::SortTable.](imapitable-sorttable.md)
    
5. Вызовите **IMAPITable::QueryRows,** чтобы получить соответствующие строки. Дополнительные сведения см. в [подразделе IMAPITable::QueryRows.](imapitable-queryrows.md)
    
6. Вызовите метод **IMAPIProp::OpenProperty** сообщения, чтобы **PR_RTF_COMPRESSED** с **интерфейсом IStream.** Дополнительные сведения см. в подразделе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED.**
    
7. Сканируйте поток, ищите замещатель отрисовки. `\objattph` Символ, следующий за этим местом, — это место для следующего вложения в отсортданной таблице.
    

