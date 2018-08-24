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
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594560"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Добавление сведений об отображении к форматированному тексту

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы указать расположение в форматированного текста, в которой отображается вложения, необходимо вставить последовательности символов заполнителя в свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Последовательность заполнитель включает в себя следующие символы: `\objattph`.
  
 **Чтобы добавить сведения о визуализации форматированный текст сообщения**
  
- При записи в потоке текста сообщения **PR_RTF_COMPRESSED** свойство, вставьте последовательность заполнитель и пробел в позиции, где должны отображаться вложение. 
    
- Присвойте свойству **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) каждого вложения в числовое значение. Минимальное значение должна быть назначена свойству **PR_RENDERING_POSITION** первого вложения в поля форматированного текста. Наибольшее значение для последнего вложения. 
    

