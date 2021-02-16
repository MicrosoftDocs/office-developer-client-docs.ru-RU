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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417373"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="15762-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="15762-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="15762-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15762-105">Получает сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="15762-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="15762-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15762-106">Parameters</span></span>

 <span data-ttu-id="15762-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="15762-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="15762-108">[out] Битоваяmas, указывающая, поддерживает ли папка общий доступ.</span><span class="sxs-lookup"><span data-stu-id="15762-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="15762-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="15762-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="15762-110">Указывает, что папка не поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="15762-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="15762-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="15762-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="15762-112">Указывает, что папка поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="15762-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15762-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15762-113">Return value</span></span>

<span data-ttu-id="15762-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="15762-114">S_OK</span></span> 
  
> <span data-ttu-id="15762-115">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="15762-115">The call was successful.</span></span>
    

