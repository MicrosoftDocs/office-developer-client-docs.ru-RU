---
title: Добавление данных отображения к форматированному тексту
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
# <a name="adding-rendering-information-to-formatted-text"></a>Добавление данных отображения к форматированному тексту

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы указать расположение в форматированном тексте, в котором отображается вложение, необходимо вставить последовательность символов заполнителя в свойство **PR_RTF_COMPRESSED** сообщения ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Последовательность заполнитель состоит из следующих символов: `\objattph`.
  
 **Добавление сведений об отображении к форматированному тексту сообщения**
  
- При записи потока текста в свойство **PR_RTF_COMPRESSED** сообщения Вставьте последовательность символов и пробел в позицию, где должно быть визуализировано вложение. 
    
- Задайте для свойства **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) каждого вложения числовое значение. Наименьшее значение должно быть назначено свойству **PR_RENDERING_POSITION** первого вложения, которое отображается в форматированном тексте; наибольшее значение последнего вложения. 
    

