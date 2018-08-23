---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579845"
---
# <a name="sync"></a><span data-ttu-id="3e9c0-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="3e9c0-103">SYNC</span></span>

  
  
<span data-ttu-id="3e9c0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e9c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e9c0-105">Сведения о запуске синхронизации между локального хранилища и сервером.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="3e9c0-106">Эти сведения используются во время [синхронизации состояния](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="3e9c0-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3e9c0-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3e9c0-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="3e9c0-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e9c0-108">Members</span></span>

 <span data-ttu-id="3e9c0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e9c0-109">_ulFlags_</span></span>
  
- <span data-ttu-id="3e9c0-110">[out] и [in] Битовая следующие флаги, изменяющего поведение во время синхронизации:</span><span class="sxs-lookup"><span data-stu-id="3e9c0-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="3e9c0-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="3e9c0-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="3e9c0-112">[in] Клиент будут выполнять только отправить.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="3e9c0-113">Outlook возвращает только локально измененное папок.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="3e9c0-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="3e9c0-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="3e9c0-115">[in] Клиент будут выполнять только файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="3e9c0-116">Outlook не должно очищать отправляемых битов для папок.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="3e9c0-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="3e9c0-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="3e9c0-118">[in] Клиент синхронизации указанный набор папок с указанным запись идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="3e9c0-119">Этот флаг может использоваться совместно с либо **UPS_UPLOAD_ONLY** , либо **UPS_DNLOAD_ONLY** флаг.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="3e9c0-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="3e9c0-120">UPS_OK</span></span>
    
  - <span data-ttu-id="3e9c0-121">[out] Синхронизация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="3e9c0-122">Клиент устанавливает это после отправки или завершения полной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="3e9c0-123">Несмотря на то, что клиент может отправить или полную синхронизацию (отправка и загрузка) папкам и элементам с помощью API репликации клиента указывает *ulFlags* с только в одном направлении репликации за раз, либо **UPS_UPLOAD_ONLY** или Флаг **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="3e9c0-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="3e9c0-124">В случае полной синхронизации клиент не сначала отправляемых с флагом **UPS_UPLOAD_ONLY** и загрузка с флагом **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="3e9c0-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="3e9c0-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="3e9c0-125">_pwzPath_</span></span>
  
- <span data-ttu-id="3e9c0-126">[out] Путь к локальному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="3e9c0-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="3e9c0-127">_Reserved1_</span></span>
  
- <span data-ttu-id="3e9c0-128">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3e9c0-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="3e9c0-129">_Reserved2_</span></span>
  
- <span data-ttu-id="3e9c0-130">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3e9c0-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="3e9c0-131">*pel*</span></span> 
  
- <span data-ttu-id="3e9c0-132">[in] Это список запись идентификаторы папки для синхронизации, если были установлены **UPS_THESE_FOLDERS** .</span><span class="sxs-lookup"><span data-stu-id="3e9c0-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="3e9c0-133">В разделе mapidefs.h для определения типа **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="3e9c0-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="3e9c0-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="3e9c0-135">[in] Если были установлены **UPS_THESE_FOLDERS** это массив параметров папки для соответствующих папок в *языке выражений PerformancePoint* .</span><span class="sxs-lookup"><span data-stu-id="3e9c0-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="3e9c0-136">Эти параметры папки используются при загрузке каждой из папок, перечисленных в *языке выражений PerformancePoint* во время [загрузки состояние папки](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="3e9c0-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="3e9c0-137">Дополнительные сведения о параметрах папки можно **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="3e9c0-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3e9c0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="3e9c0-138">See also</span></span>



[<span data-ttu-id="3e9c0-139">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="3e9c0-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3e9c0-140">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="3e9c0-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3e9c0-141">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3e9c0-141">MAPI Constants</span></span>](mapi-constants.md)

