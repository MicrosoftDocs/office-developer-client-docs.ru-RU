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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331124"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="9df5b-103">Добавление данных отображения к форматированному тексту</span><span class="sxs-lookup"><span data-stu-id="9df5b-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="9df5b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9df5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9df5b-105">Чтобы указать расположение в форматированном тексте, в котором отображается вложение, необходимо вставить последовательность замещающих символов в свойство сообщения **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9df5b-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="9df5b-106">Последовательность заполнитель состоит из следующих символов: `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="9df5b-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="9df5b-107">**Добавление сведений об отображении к форматированному тексту сообщения**</span><span class="sxs-lookup"><span data-stu-id="9df5b-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="9df5b-108">При записи потока текста в свойство **пр_ртф_компрессед** сообщения Вставьте последовательность символов и пробел в позицию, где должно быть визуализировано вложение.</span><span class="sxs-lookup"><span data-stu-id="9df5b-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="9df5b-109">ПриСвойте свойству **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) каждого вложения числовое значение.</span><span class="sxs-lookup"><span data-stu-id="9df5b-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="9df5b-110">Минимальное значение должно быть назначено свойству **пр_рендеринг_поситион** первого вложения, которое отображается в форматированном тексте; наибольшее значение последнего вложения.</span><span class="sxs-lookup"><span data-stu-id="9df5b-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

