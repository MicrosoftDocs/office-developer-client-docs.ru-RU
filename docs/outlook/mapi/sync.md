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
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433810"
---
# <a name="sync"></a><span data-ttu-id="a5c5b-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="a5c5b-103">SYNC</span></span>

  
  
<span data-ttu-id="a5c5b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5c5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5c5b-105">Сведения о запуске синхронизации между локальным хранилищем и сервером.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="a5c5b-106">Эти сведения используются в [состоянии синхронизации](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="a5c5b-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a5c5b-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a5c5b-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a5c5b-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a5c5b-108">Members</span></span>

 <span data-ttu-id="a5c5b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5c5b-109">_ulFlags_</span></span>
  
- <span data-ttu-id="a5c5b-110">[out]/[in] битовая маска следующих флагов, которые изменяют поведение во время синхронизации:</span><span class="sxs-lookup"><span data-stu-id="a5c5b-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="a5c5b-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5c5b-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="a5c5b-112">возврата Клиент будет выполнять только отправку.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="a5c5b-113">Outlook возвращает только локальные измененные папки.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="a5c5b-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5c5b-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="a5c5b-115">возврата Клиент будет выполнять только загрузку.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="a5c5b-116">Outlook не должен очищать биты отправки для папок.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="a5c5b-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="a5c5b-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="a5c5b-118">возврата Клиент будет синхронизировать заданный набор папок с указанными идентификаторами записи.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="a5c5b-119">Этот флаг можно сочетать с флагом **UPS_UPLOAD_ONLY** или **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="a5c5b-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="a5c5b-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="a5c5b-120">UPS_OK</span></span>
    
  - <span data-ttu-id="a5c5b-121">вышли Синхронизация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="a5c5b-122">Клиент устанавливает это после отправки или завершения полной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="a5c5b-123">Несмотря на то, что клиент может загружать или полностью синхронизировать (загрузить, а затем загружать) папки и элементы с помощью API репликации, клиент указывает *ulFlags* с одним направлением репликации одновременно — либо с помощью флага **UPS_UPLOAD_ONLY** , либо **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="a5c5b-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="a5c5b-124">В случае полной синхронизации клиент сначала выполняет отправку с флагом **UPS_UPLOAD_ONLY** , а затем загружается с флагом **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="a5c5b-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="a5c5b-125">_пвзпас_</span><span class="sxs-lookup"><span data-stu-id="a5c5b-125">_pwzPath_</span></span>
  
- <span data-ttu-id="a5c5b-126">вышли Путь к локальному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="a5c5b-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="a5c5b-127">_Reserved1_</span></span>
  
- <span data-ttu-id="a5c5b-128">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a5c5b-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="a5c5b-129">_Reserved2_</span></span>
  
- <span data-ttu-id="a5c5b-130">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a5c5b-131">*выражений*</span><span class="sxs-lookup"><span data-stu-id="a5c5b-131">*pel*</span></span> 
  
- <span data-ttu-id="a5c5b-132">возврата Это список идентификаторов записей для синхронизации, если **UPS_THESE_FOLDERS** задано.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="a5c5b-133">Определение типа **лпентрилист**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="a5c5b-134">_пулфолдероптионс_</span><span class="sxs-lookup"><span data-stu-id="a5c5b-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="a5c5b-135">возврата Это массив свойств папки для соответствующих папок в *PEL* , если **UPS_THESE_FOLDERS** задано.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="a5c5b-136">Эти параметры папки используются при отправке каждой из папок, перечисленных в *PEL* , в [состояние папки отправки](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="a5c5b-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="a5c5b-137">Для получения дополнительных сведений о параметрах папки обратитесь к разделу **[упфлд](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="a5c5b-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a5c5b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a5c5b-138">See also</span></span>



[<span data-ttu-id="a5c5b-139">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a5c5b-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a5c5b-140">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a5c5b-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a5c5b-141">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="a5c5b-141">MAPI Constants</span></span>](mapi-constants.md)

