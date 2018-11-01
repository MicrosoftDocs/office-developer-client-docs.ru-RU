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
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572293"
---
# <a name="upfld"></a><span data-ttu-id="1222b-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="1222b-103">UPFLD</span></span>

<span data-ttu-id="1222b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1222b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1222b-105">Сведения для передачи в папку во время [загрузки состояние папки](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="1222b-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1222b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1222b-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="1222b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1222b-107">Members</span></span>

<span data-ttu-id="1222b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1222b-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="1222b-109">[out] и [in] флаги для определения соответствующих действий для uplaod.</span><span class="sxs-lookup"><span data-stu-id="1222b-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="1222b-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="1222b-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="1222b-111">[out] Папка является новым.</span><span class="sxs-lookup"><span data-stu-id="1222b-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="1222b-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="1222b-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="1222b-113">[out] Папка была перемещена.</span><span class="sxs-lookup"><span data-stu-id="1222b-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="1222b-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="1222b-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="1222b-115">[out] Свойства папки были изменены.</span><span class="sxs-lookup"><span data-stu-id="1222b-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="1222b-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="1222b-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="1222b-117">[out] Папка была удалена.</span><span class="sxs-lookup"><span data-stu-id="1222b-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="1222b-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="1222b-118">UPF_OK</span></span>
    
    - <span data-ttu-id="1222b-119">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="1222b-119">[in] Upload was successful.</span></span> <span data-ttu-id="1222b-120">Клиент устанавливает это после отправки сведений о папке на сервере.</span><span class="sxs-lookup"><span data-stu-id="1222b-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="1222b-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="1222b-121">_pfld_</span></span>
  
> <span data-ttu-id="1222b-122">[out] Объект открыть папку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="1222b-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="1222b-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="1222b-123">_feid_</span></span>
  
> <span data-ttu-id="1222b-124">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="1222b-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1222b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1222b-125">See also</span></span>

- [<span data-ttu-id="1222b-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="1222b-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="1222b-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="1222b-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1222b-128">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="1222b-128">MAPI Constants</span></span>](mapi-constants.md)

