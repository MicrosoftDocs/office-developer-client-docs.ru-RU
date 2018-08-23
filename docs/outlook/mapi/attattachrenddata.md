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
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569451"
---
# <a name="attattachrenddata"></a><span data-ttu-id="7e7e8-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="7e7e8-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="7e7e8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e7e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e7e8-105">Атрибут **attAttachRenddata** закодирован структура **RENDDATA** , описывается, как и где вложения отображается в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="7e7e8-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="7e7e8-106">Структура **RENDDATA** просто кодируется в потоке TNEF **sizeof(RENDDATA)** байт, начиная с первого элемента структуры **RENDDATA** .</span><span class="sxs-lookup"><span data-stu-id="7e7e8-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="7e7e8-107">Если участник **dwFlags** структура **RENDDATA** имеет значение **MAC_BINARY**, затем данные для следующих вложения хранятся в файлы формата; в противном случае данные вложения кодируются как обычно.</span><span class="sxs-lookup"><span data-stu-id="7e7e8-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

