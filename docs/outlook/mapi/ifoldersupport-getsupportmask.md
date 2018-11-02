---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567855"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="bc480-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="bc480-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="bc480-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc480-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc480-105">Получает сведения о поддержке папки для совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="bc480-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="bc480-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc480-106">Parameters</span></span>

 <span data-ttu-id="bc480-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="bc480-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="bc480-108">[out] Битовая маска, указывающее, поддерживает ли общий доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="bc480-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="bc480-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="bc480-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="bc480-110">Указывает, что папка не поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="bc480-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="bc480-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="bc480-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="bc480-112">Указывает, что папка поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="bc480-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc480-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc480-113">Return value</span></span>

<span data-ttu-id="bc480-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc480-114">S_OK</span></span> 
  
> <span data-ttu-id="bc480-115">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bc480-115">The call was successful.</span></span>
    

