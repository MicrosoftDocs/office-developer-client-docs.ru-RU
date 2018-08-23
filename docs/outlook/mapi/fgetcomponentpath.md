---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa39128ffaaaa3530b74a660c14971834a99561b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566350"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="d28b6-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="d28b6-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="d28b6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d28b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d28b6-105">Возвращает путь к частной Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d28b6-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="d28b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d28b6-106">Parameters</span></span>

 <span data-ttu-id="d28b6-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="d28b6-107">_szComponent_</span></span>
  
> <span data-ttu-id="d28b6-108">[in] Раздел реестра MSIComponentID, описанные в [Параметры реестра заглушка Mapi32.dll](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="d28b6-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="d28b6-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="d28b6-109">_szQualifier_</span></span>
  
> <span data-ttu-id="d28b6-110">[in] Подраздел MSIApplicationLCID или MSIOfficeLCID, описанных в [выберите определенные версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="d28b6-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="d28b6-111">Вызывающие объекты можно передать **значение null** , если нет квантор.</span><span class="sxs-lookup"><span data-stu-id="d28b6-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="d28b6-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="d28b6-112">_szDllPath_</span></span>
  
> <span data-ttu-id="d28b6-113">[in] Путь к частной Mapi32.dll, имеющем полной функциональности MAPI (же экспортирует в виде Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="d28b6-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="d28b6-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="d28b6-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="d28b6-115">[in] Размер _szDllPath_, в символы.</span><span class="sxs-lookup"><span data-stu-id="d28b6-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="d28b6-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="d28b6-116">_fInstall_</span></span>
  
> <span data-ttu-id="d28b6-117">[in] Указывает MAPI для установки частный Mapi32.dll компонент, если он отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d28b6-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d28b6-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d28b6-118">Return value</span></span>

 <span data-ttu-id="d28b6-119">**значение true**</span><span class="sxs-lookup"><span data-stu-id="d28b6-119">**true**</span></span>
  
> <span data-ttu-id="d28b6-120">Найти путь.</span><span class="sxs-lookup"><span data-stu-id="d28b6-120">The path was found.</span></span>
    
 <span data-ttu-id="d28b6-121">**false**</span><span class="sxs-lookup"><span data-stu-id="d28b6-121">**false**</span></span>
  
> <span data-ttu-id="d28b6-122">Путь не найден.</span><span class="sxs-lookup"><span data-stu-id="d28b6-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d28b6-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="d28b6-123">Remarks</span></span>

<span data-ttu-id="d28b6-124">Используйте функцию **FGetComponentPath** , если вам нужно получить путь к частной Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d28b6-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d28b6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d28b6-125">See also</span></span>



[<span data-ttu-id="d28b6-126">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="d28b6-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="d28b6-127">Параметры реестра заглушка Mapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d28b6-127">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

