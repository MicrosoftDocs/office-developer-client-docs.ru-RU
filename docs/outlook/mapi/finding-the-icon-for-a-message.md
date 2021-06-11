---
title: Поиск значка для сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409155"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="c9062-103">Поиск значка для сообщения</span><span class="sxs-lookup"><span data-stu-id="c9062-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="c9062-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9062-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c9062-105">**Поиск значка, связанного с сообщением**</span><span class="sxs-lookup"><span data-stu-id="c9062-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="c9062-106">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) **для** получения свойства PR_MESSAGE_CLASS [(PidTagMessageClass).](pidtagmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c9062-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="c9062-107">Вызов [MAPIOpenFormMgr для](mapiopenformmgr.md) получения **указателя интерфейса IMAPIFormMgr.**</span><span class="sxs-lookup"><span data-stu-id="c9062-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="c9062-108">**Передай указатель IMAPISession** в _параметре pSession._</span><span class="sxs-lookup"><span data-stu-id="c9062-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="c9062-109">Вызов [IMAPIFormMgr::ResolveMessageClass,](imapiformmgr-resolvemessageclass.md) чтобы получить **указатель интерфейса IMAPIFormInfo.**</span><span class="sxs-lookup"><span data-stu-id="c9062-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="c9062-110">Используйте указатель **IMAPIFormInfo** для вызова [свойств IMAPIProp::GetProps](imapiprop-getprops.md) и получения свойств PR_ICON [(PidTagIcon)](pidtagicon-canonical-property.md)и/или **PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="c9062-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

