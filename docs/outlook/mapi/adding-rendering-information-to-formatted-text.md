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
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="42af4-103">Добавление сведений об отображении к форматированному тексту</span><span class="sxs-lookup"><span data-stu-id="42af4-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="42af4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42af4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42af4-105">Чтобы указать расположение в форматированного текста, в которой отображается вложения, необходимо вставить последовательности символов заполнителя в свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="42af4-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="42af4-106">Последовательность заполнитель включает в себя следующие символы: `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="42af4-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="42af4-107">**Чтобы добавить сведения о визуализации форматированный текст сообщения**</span><span class="sxs-lookup"><span data-stu-id="42af4-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="42af4-108">При записи в потоке текста сообщения **PR_RTF_COMPRESSED** свойство, вставьте последовательность заполнитель и пробел в позиции, где должны отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="42af4-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="42af4-109">Присвойте свойству **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) каждого вложения в числовое значение.</span><span class="sxs-lookup"><span data-stu-id="42af4-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="42af4-110">Минимальное значение должна быть назначена свойству **PR_RENDERING_POSITION** первого вложения в поля форматированного текста. Наибольшее значение для последнего вложения.</span><span class="sxs-lookup"><span data-stu-id="42af4-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

