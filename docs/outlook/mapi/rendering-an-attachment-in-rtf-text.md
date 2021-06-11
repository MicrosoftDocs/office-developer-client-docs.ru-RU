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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты с богатым текстовым форматом (RTF) могут получать сведения о позиции отрисовки из  текста сообщения RTF, ищем следующую последовательность побега в свойстве PR_RTF_COMPRESSED сообщения[(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)
  
 `\objattph`
  
 **Поиск сведений о отрисовки в форматированный текст**
  
1. Позвоните **в IMessage::GetAttachmentTable,** чтобы получить доступ к таблице вложений сообщения. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Создайте ограничение свойства, ограничивающее таблицу строками, **PR_RENDERING_POSITION** не равными -1. Дополнительные сведения см. **в PR_RENDERING_POSITION** [(PidTagRenderingPosition).](pidtagrenderingposition-canonical-property.md)
    
3. Call **IMAPITable:::Restrict** to enforce the restriction. Дополнительные сведения см. [в iMAPITable::Restrict](imapitable-restrict.md).
    
4. Вызов **IMAPITable::SortTable для** сортировки вложений. Дополнительные сведения см. [в iMAPITable::SortTable](imapitable-sorttable.md).
    
5. Вызов **IMAPITable::QueryRows,** чтобы получить соответствующие строки. Дополнительные сведения см. [в iMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Вызовите метод **IMAPIProp::OpenProperty** для  получения PR_RTF_COMPRESSED **интерфейса IStream.** Дополнительные сведения см. [в iMAPIProp::OpenProperty](imapiprop-openproperty.md) **и PR_RTF_COMPRESSED.**
    
7. Сканируйте поток, ищите местообладатель отрисовки. `\objattph` Символ, следующий за этим местом, — это место для следующего вложения в сортировке таблицы.
    

