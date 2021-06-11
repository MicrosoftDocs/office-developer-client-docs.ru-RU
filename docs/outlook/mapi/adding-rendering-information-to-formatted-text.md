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
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="74f48-103">Добавление сведений о отрисовки в форматированный текст</span><span class="sxs-lookup"><span data-stu-id="74f48-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="74f48-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74f48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74f48-105">Чтобы указать расположение в форматированный текст, в котором отрисовка вложения, необходимо  вставить последовательность символов-задатков в свойство[PR_RTF_COMPRESSED (PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="74f48-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="74f48-106">Последовательность задатки состоит из следующих символов:  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="74f48-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="74f48-107">**Добавление данных отрисовки в форматированный текст сообщения**</span><span class="sxs-lookup"><span data-stu-id="74f48-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="74f48-108">При записи потока текста в свойство PR_RTF_COMPRESSED сообщения **вставьте** последовательность и символ пространства в положение, в котором должно быть отрисовка вложения.</span><span class="sxs-lookup"><span data-stu-id="74f48-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="74f48-109">Установите **свойство PR_RENDERING_POSITION** [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)каждого вложения к числовому значению.</span><span class="sxs-lookup"><span data-stu-id="74f48-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="74f48-110">Наименьшее значение должно быть назначено свойству **PR_RENDERING_POSITION** первого вложения, появляемого в отформатированный текст; самое высокое значение для последнего вложения.</span><span class="sxs-lookup"><span data-stu-id="74f48-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

