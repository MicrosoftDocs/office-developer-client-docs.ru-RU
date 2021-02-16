---
title: Добавление сведений об отрисовки в форматированный текст
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
# <a name="adding-rendering-information-to-formatted-text"></a>Добавление сведений об отрисовки в форматированный текст

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы указать расположение в форматном тексте, в котором отрисовка вложения, необходимо вставить последовательность символов-замещений в свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) Последовательность-замесь состоит из следующих символов:  `\objattph` .
  
 **Добавление сведений об отобращении в форматированный текст сообщения**
  
- При записи потока текста в  свойство PR_RTF_COMPRESSED вставьте последовательность-замещение и пробел в положение, где должно быть отрисовлено вложение. 
    
- Зада **PR_RENDERING_POSITION** ([PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)каждого вложения в числовом значении. Минимальное значение должно быть  назначено свойству PR_RENDERING_POSITION первого вложения, чтобы отформатированный текст; самое высокое значение последнего вложения. 
    

