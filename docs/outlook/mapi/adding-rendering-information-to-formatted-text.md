---
title: Добавление сведений об отображении к форматированному тексту
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808019"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Добавление сведений об отображении к форматированному тексту

  
  
**Относится к**: Outlook 
  
Чтобы указать расположение в форматированного текста, в которой отображается вложения, необходимо вставить последовательности символов заполнителя в свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Последовательность заполнитель включает в себя следующие символы: `\objattph`.
  
 **Чтобы добавить сведения о визуализации форматированный текст сообщения**
  
- При записи в потоке текста сообщения **PR_RTF_COMPRESSED** свойство, вставьте последовательность заполнитель и пробел в позиции, где должны отображаться вложение. 
    
- Присвойте свойству **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) каждого вложения в числовое значение. Минимальное значение должна быть назначена свойству **PR_RENDERING_POSITION** первого вложения в поля форматированного текста. Наибольшее значение для последнего вложения. 
    

