---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427138"
---
# <a name="attattachrenddata"></a><span data-ttu-id="d0b86-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="d0b86-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="d0b86-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0b86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0b86-105">Атрибут **аттаттачренддата** кодируется как структура **ренддата** , описывающая способ и место отображения вложения в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0b86-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="d0b86-106">Структура **ренддата** просто кодируется в потоке TNEF как **sizeof (ренддата)** байтов, начиная с первого элемента структуры **ренддата** .</span><span class="sxs-lookup"><span data-stu-id="d0b86-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="d0b86-107">Если для элемента **dwFlags** структуры **ренддата** задано значение **мак_бинари**, то данные для следующего вложения хранятся в формате макбинари; в противном случае данные вложения кодируются как обычно.</span><span class="sxs-lookup"><span data-stu-id="d0b86-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

