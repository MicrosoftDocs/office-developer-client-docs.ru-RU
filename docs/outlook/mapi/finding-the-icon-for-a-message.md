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
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567813"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="31852-103">Поиск значка сообщения</span><span class="sxs-lookup"><span data-stu-id="31852-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="31852-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31852-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="31852-105">**Чтобы найти значка, сопоставленного с сообщением**</span><span class="sxs-lookup"><span data-stu-id="31852-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="31852-106">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) сообщений для получения его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31852-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="31852-107">Вызов [MAPIOpenFormMgr](mapiopenformmgr.md) для получения указателя интерфейса **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="31852-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="31852-108">Передайте указатель **IMAPISession** с помощью параметра _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="31852-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="31852-109">Вызов [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения указателя интерфейса **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="31852-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="31852-110">С помощью **IMAPIFormInfo** указателя Позвонить [IMAPIProp::GetProps](imapiprop-getprops.md) и получить **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и/или свойства **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31852-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

