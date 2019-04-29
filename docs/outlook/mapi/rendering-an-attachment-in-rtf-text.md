---
title: Отображение вложения в тексте в формате RTF
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
# <a name="rendering-an-attachment-in-rtf-text"></a>Отображение вложения в тексте в формате RTF

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты, поддерживающие формат RTF, могут получать сведения о позициях отображения из текста сообщений в формате RTF, найдя следующую escape-последовательность в свойстве **пр_ртф_компрессед** сообщения ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):
  
 `\objattph`
  
 **Размещение информации для отображения в форматированном тексте**
  
1. Call **iMessage:: жетаттачменттабле** для доступа к таблице вложений сообщения. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Создайте ограничение свойства, которое ограничит таблицу строками, у которых значение параметра **пр_рендеринг_поситион** не равно – 1. Дополнительные сведения см. в статье **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Вызов **IMAPITable:: Ограничьте** для применения ограничения. Для получения дополнительных сведений обратитесь к разделу [IMAPITable:: restrict](imapitable-restrict.md).
    
4. Call **IMAPITable:: сорттабле** для сортировки вложений. Дополнительные сведения см. в разделе [IMAPITable:: сорттабле](imapitable-sorttable.md).
    
5. Call **IMAPITable:: QueryRows** для получения соответствующих строк. Дополнительные сведения см. в разделе [IMAPITable:: QueryRows](imapitable-queryrows.md).
    
6. ВыЗовите метод **IMAPIProp:: опенпроперти** , чтобы получить **пр_ртф_компрессед** с интерфейсом **IStream** . Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и **пр_ртф_компрессед**.
    
7. ПроСканируйте поток, выполняя поиск заполнителя отображения `\objattph`,. Символ после этого заполнителя — это место для следующего вложения в таблице сортировки.
    

