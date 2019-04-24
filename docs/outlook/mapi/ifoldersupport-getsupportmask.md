---
title: Ифолдерсуппортжетсуппортмаск
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350836"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="f0a0e-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="f0a0e-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="f0a0e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0a0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0a0e-105">Получает сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f0a0e-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="f0a0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0a0e-106">Parameters</span></span>

 <span data-ttu-id="f0a0e-107">_Пдвсуппортмаск_</span><span class="sxs-lookup"><span data-stu-id="f0a0e-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="f0a0e-108">вышли Битовая маска, указывающая, поддерживает ли папка общий доступ.</span><span class="sxs-lookup"><span data-stu-id="f0a0e-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="f0a0e-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="f0a0e-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="f0a0e-110">Указывает, что папка не поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="f0a0e-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="f0a0e-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="f0a0e-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="f0a0e-112">Указывает, что папка поддерживает общий доступ.</span><span class="sxs-lookup"><span data-stu-id="f0a0e-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0a0e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0a0e-113">Return value</span></span>

<span data-ttu-id="f0a0e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0a0e-114">S_OK</span></span> 
  
> <span data-ttu-id="f0a0e-115">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f0a0e-115">The call was successful.</span></span>
    

