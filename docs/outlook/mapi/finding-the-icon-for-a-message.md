---
title: Поиск значка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808426"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="41dbd-103">Поиск значка сообщения</span><span class="sxs-lookup"><span data-stu-id="41dbd-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="41dbd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41dbd-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="41dbd-105">**Чтобы найти значка, сопоставленного с сообщением**</span><span class="sxs-lookup"><span data-stu-id="41dbd-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="41dbd-106">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) сообщений для получения его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41dbd-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="41dbd-107">Вызов [MAPIOpenFormMgr](mapiopenformmgr.md) для получения указателя интерфейса **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="41dbd-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="41dbd-108">Передайте указатель **IMAPISession** с помощью параметра _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="41dbd-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="41dbd-109">Вызов [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения указателя интерфейса **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="41dbd-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="41dbd-110">С помощью **IMAPIFormInfo** указателя Позвонить [IMAPIProp::GetProps](imapiprop-getprops.md) и получить **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и/или свойства **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41dbd-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

