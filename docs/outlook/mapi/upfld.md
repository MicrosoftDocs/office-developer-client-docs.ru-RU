---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431360"
---
# <a name="upfld"></a><span data-ttu-id="59233-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="59233-103">UPFLD</span></span>

<span data-ttu-id="59233-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59233-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59233-105">Сведения о загрузке папки во время состояния [папки загрузки.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="59233-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="59233-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="59233-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="59233-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="59233-107">Members</span></span>

<span data-ttu-id="59233-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59233-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="59233-109">[out]/[in] Флаги для определения соответствующих действий для uplaod.</span><span class="sxs-lookup"><span data-stu-id="59233-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="59233-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="59233-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="59233-111">[вышел] Папка новая.</span><span class="sxs-lookup"><span data-stu-id="59233-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="59233-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="59233-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="59233-113">[вышел] Папка перемещена.</span><span class="sxs-lookup"><span data-stu-id="59233-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="59233-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="59233-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="59233-115">[вышел] Изменены свойства папок.</span><span class="sxs-lookup"><span data-stu-id="59233-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="59233-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="59233-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="59233-117">[вышел] Папка была удалена.</span><span class="sxs-lookup"><span data-stu-id="59233-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="59233-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="59233-118">UPF_OK</span></span>
    
    - <span data-ttu-id="59233-119">[in] Upload успешно.</span><span class="sxs-lookup"><span data-stu-id="59233-119">[in] Upload was successful.</span></span> <span data-ttu-id="59233-120">Клиент задает это после отправки данных папок на сервер.</span><span class="sxs-lookup"><span data-stu-id="59233-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="59233-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="59233-121">_pfld_</span></span>
  
> <span data-ttu-id="59233-122">[вышел] Объект открытой папки для загрузки.</span><span class="sxs-lookup"><span data-stu-id="59233-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="59233-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="59233-123">_feid_</span></span>
  
> <span data-ttu-id="59233-124">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="59233-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59233-125">См. также</span><span class="sxs-lookup"><span data-stu-id="59233-125">See also</span></span>

- [<span data-ttu-id="59233-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="59233-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="59233-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="59233-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="59233-128">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="59233-128">MAPI Constants</span></span>](mapi-constants.md)

