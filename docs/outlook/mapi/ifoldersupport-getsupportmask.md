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
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808813"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="4e165-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="4e165-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="4e165-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e165-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e165-105">Получает сведения о поддержке папки для совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="4e165-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="4e165-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e165-106">Parameters</span></span>

 <span data-ttu-id="4e165-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="4e165-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="4e165-108">[out] Битовая маска, указывающее, поддерживает ли общий доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="4e165-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="4e165-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="4e165-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="4e165-110">Указывает, что папка не поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="4e165-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="4e165-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="4e165-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="4e165-112">Указывает, что папка поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="4e165-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e165-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4e165-113">Return value</span></span>

<span data-ttu-id="4e165-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4e165-114">S_OK</span></span> 
  
> <span data-ttu-id="4e165-115">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4e165-115">The call was successful.</span></span>
    

