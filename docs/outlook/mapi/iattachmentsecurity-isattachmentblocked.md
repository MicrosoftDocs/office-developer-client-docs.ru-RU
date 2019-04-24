---
title: Иаттачментсекуритисаттачментблоккед
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
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350850"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="a3d37-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="a3d37-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="a3d37-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3d37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3d37-105">Проверяет, блокируется ли указанное вложение приложением Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="a3d37-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="a3d37-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3d37-106">Parameters</span></span>

 <span data-ttu-id="a3d37-107">_Пвсзфиленаме_</span><span class="sxs-lookup"><span data-stu-id="a3d37-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="a3d37-108">возврата Указатель на имя файла вложения.</span><span class="sxs-lookup"><span data-stu-id="a3d37-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="a3d37-109">_Пфблоккед_</span><span class="sxs-lookup"><span data-stu-id="a3d37-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="a3d37-110">вышли Указатель на значение **true** , если указанное вложение заблокировано; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="a3d37-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3d37-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a3d37-111">See also</span></span>



[<span data-ttu-id="a3d37-112">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="a3d37-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a3d37-113">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="a3d37-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

