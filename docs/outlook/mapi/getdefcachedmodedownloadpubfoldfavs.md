---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808566"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="e7067-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="e7067-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="e7067-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7067-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7067-105">Указывает, включена ли режима кэширования данных Exchange для **Общей папки "Избранное"** папки и ли это требование политики.</span><span class="sxs-lookup"><span data-stu-id="e7067-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e7067-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e7067-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7067-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="e7067-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e7067-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e7067-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e7067-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e7067-109">Called by:</span></span>  <br/> |<span data-ttu-id="e7067-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="e7067-110">Client</span></span>  <br/> |
|<span data-ttu-id="e7067-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e7067-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7067-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e7067-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="e7067-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="e7067-113">Parameters</span></span>

 <span data-ttu-id="e7067-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="e7067-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="e7067-115">[out] **значение true,** Если возвращаемое значение обеспечивается политики **значение false** , если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="e7067-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e7067-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e7067-116">Return values</span></span>

 <span data-ttu-id="e7067-117">**значение true**</span><span class="sxs-lookup"><span data-stu-id="e7067-117">**true**</span></span>
  
- <span data-ttu-id="e7067-118">Кэширование.</span><span class="sxs-lookup"><span data-stu-id="e7067-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="e7067-119">**false**</span><span class="sxs-lookup"><span data-stu-id="e7067-119">**false**</span></span>
  
- <span data-ttu-id="e7067-120">Кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="e7067-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7067-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e7067-121">See also</span></span>



[<span data-ttu-id="e7067-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="e7067-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

