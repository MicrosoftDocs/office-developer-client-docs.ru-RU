---
title: Добавление сведений о отрисовки в форматированный текст
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420614"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Добавление сведений о отрисовки в форматированный текст

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы указать расположение в форматированный текст, в котором отрисовка вложения, необходимо  вставить последовательность символов-задатков в свойство[PR_RTF_COMPRESSED (PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) Последовательность задатки состоит из следующих символов:  `\objattph` .
  
 **Добавление данных отрисовки в форматированный текст сообщения**
  
- При записи потока текста в свойство PR_RTF_COMPRESSED сообщения **вставьте** последовательность и символ пространства в положение, в котором должно быть отрисовка вложения. 
    
- Установите **свойство PR_RENDERING_POSITION** [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)каждого вложения к числовому значению. Наименьшее значение должно быть назначено свойству **PR_RENDERING_POSITION** первого вложения, появляемого в отформатированный текст; самое высокое значение для последнего вложения. 
    

