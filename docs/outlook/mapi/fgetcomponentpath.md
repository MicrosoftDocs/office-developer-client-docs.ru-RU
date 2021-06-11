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
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335212"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="01d57-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="01d57-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="01d57-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d57-105">Возвращает путь к частному Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="01d57-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="01d57-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="01d57-106">Parameters</span></span>

 <span data-ttu-id="01d57-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="01d57-107">_szComponent_</span></span>
  
> <span data-ttu-id="01d57-108">[in] Ключ reg MSIComponentID, описанный вMapi32.dll [реестра Stub Параметры](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="01d57-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="01d57-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="01d57-109">_szQualifier_</span></span>
  
> <span data-ttu-id="01d57-110">[in] Подкайка MSIApplicationLCID или MSIOfficeLCID, описанная в "Выбор определенной версии [MAPI для загрузки".](how-to-choose-a-specific-version-of-mapi-to-load.md)</span><span class="sxs-lookup"><span data-stu-id="01d57-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="01d57-111">Если нет квалификатора, звонители могут передать **null.**</span><span class="sxs-lookup"><span data-stu-id="01d57-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="01d57-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="01d57-112">_szDllPath_</span></span>
  
> <span data-ttu-id="01d57-113">[in] Путь к частному Mapi32.dll, который имеет полный функционал MAPI (тот же экспорт, что и Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="01d57-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="01d57-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="01d57-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="01d57-115">[in] Размер  _szDllPath_ в символах.</span><span class="sxs-lookup"><span data-stu-id="01d57-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="01d57-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="01d57-116">_fInstall_</span></span>
  
> <span data-ttu-id="01d57-117">[in] Сообщает MAPI установить частный компонент Mapi32.dll, если он отсутствует.</span><span class="sxs-lookup"><span data-stu-id="01d57-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01d57-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01d57-118">Return value</span></span>

 <span data-ttu-id="01d57-119">**true**</span><span class="sxs-lookup"><span data-stu-id="01d57-119">**true**</span></span>
  
> <span data-ttu-id="01d57-120">Путь найден.</span><span class="sxs-lookup"><span data-stu-id="01d57-120">The path was found.</span></span>
    
 <span data-ttu-id="01d57-121">**false**</span><span class="sxs-lookup"><span data-stu-id="01d57-121">**false**</span></span>
  
> <span data-ttu-id="01d57-122">Путь не найден.</span><span class="sxs-lookup"><span data-stu-id="01d57-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01d57-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="01d57-123">Remarks</span></span>

<span data-ttu-id="01d57-124">Используйте **функцию FGetComponentPath** для получения пути к частному Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="01d57-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01d57-125">См. также</span><span class="sxs-lookup"><span data-stu-id="01d57-125">See also</span></span>



[<span data-ttu-id="01d57-126">Выберите определенную версию MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="01d57-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="01d57-127">Mapi32.dll реестра Stub Параметры</span><span class="sxs-lookup"><span data-stu-id="01d57-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

