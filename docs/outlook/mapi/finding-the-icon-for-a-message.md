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
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336955"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="79549-103">Поиск значка сообщения</span><span class="sxs-lookup"><span data-stu-id="79549-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="79549-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79549-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="79549-105">**Чтобы найти значок, связанный с сообщением**</span><span class="sxs-lookup"><span data-stu-id="79549-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="79549-106">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS сообщения, чтобы получить свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="79549-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="79549-107">ВыЗовите [мапиопенформмгр](mapiopenformmgr.md) , чтобы получить указатель интерфейса **имапиформмгр** .</span><span class="sxs-lookup"><span data-stu-id="79549-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="79549-108">Передайте указатель **IMAPISession** в параметр _псессион_ .</span><span class="sxs-lookup"><span data-stu-id="79549-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="79549-109">Call [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для получения указателя интерфейса **имапиформинфо** .</span><span class="sxs-lookup"><span data-stu-id="79549-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="79549-110">Используйте указатель **имапиформинфо** , чтобы вызвать [IMAPIProp::](imapiprop-getprops.md) -PROPS и извлечь свойства **пр_икон** ([PidTagIcon](pidtagicon-canonical-property.md)) и/или **пр_мини_икон** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="79549-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

