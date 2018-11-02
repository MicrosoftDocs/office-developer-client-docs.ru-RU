---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565048"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="32bc8-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="32bc8-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="32bc8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32bc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32bc8-105">Проверяет, если указанное вложение не заблокирован по Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="32bc8-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="32bc8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32bc8-106">Parameters</span></span>

 <span data-ttu-id="32bc8-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="32bc8-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="32bc8-108">[in] Указатель на имени файла вложения.</span><span class="sxs-lookup"><span data-stu-id="32bc8-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="32bc8-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="32bc8-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="32bc8-110">[out] Указатель на значение, указывающее **значение true,** Если указанное вложение блокируется. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="32bc8-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32bc8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="32bc8-111">See also</span></span>



[<span data-ttu-id="32bc8-112">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="32bc8-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="32bc8-113">Убедитесь, что Заблокированные вложения</span><span class="sxs-lookup"><span data-stu-id="32bc8-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

