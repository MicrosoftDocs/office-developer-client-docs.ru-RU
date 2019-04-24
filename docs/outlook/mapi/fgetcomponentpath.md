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
# <a name="fgetcomponentpath"></a><span data-ttu-id="34974-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="34974-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="34974-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34974-105">Возвращает путь к закрытой MAPI32. dll.</span><span class="sxs-lookup"><span data-stu-id="34974-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="34974-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34974-106">Parameters</span></span>

 <span data-ttu-id="34974-107">_Сзкомпонент_</span><span class="sxs-lookup"><span data-stu-id="34974-107">_szComponent_</span></span>
  
> <span data-ttu-id="34974-108">возврата Ключ Мсикомпонентид reg, описанный в [разделе Параметры реестра MAPI32. dll-заглушек](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="34974-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="34974-109">_Сзкуалифиер_</span><span class="sxs-lookup"><span data-stu-id="34974-109">_szQualifier_</span></span>
  
> <span data-ttu-id="34974-110">возврата Подраздел МсиаппликатионлЦид или МсиоффицелЦид, описанный в статье [Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="34974-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="34974-111">Вызывающие абоненты могут передавать **значение NULL** , если нет квалификатора.</span><span class="sxs-lookup"><span data-stu-id="34974-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="34974-112">_Сздллпас_</span><span class="sxs-lookup"><span data-stu-id="34974-112">_szDllPath_</span></span>
  
> <span data-ttu-id="34974-113">возврата Путь к частному MAPI32. dll, который имеет полную функциональность MAPI (те же экспортируемые компоненты, что и в MAPI32. dll).</span><span class="sxs-lookup"><span data-stu-id="34974-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="34974-114">_Кчбуфферсизе_</span><span class="sxs-lookup"><span data-stu-id="34974-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="34974-115">возврата Размер _сздллпас_в символах.</span><span class="sxs-lookup"><span data-stu-id="34974-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="34974-116">_Финсталл_</span><span class="sxs-lookup"><span data-stu-id="34974-116">_fInstall_</span></span>
  
> <span data-ttu-id="34974-117">возврата Указывает MAPI для установки закрытого компонента MAPI32. dll (если он отсутствует).</span><span class="sxs-lookup"><span data-stu-id="34974-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34974-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34974-118">Return value</span></span>

 <span data-ttu-id="34974-119">**относится**</span><span class="sxs-lookup"><span data-stu-id="34974-119">**true**</span></span>
  
> <span data-ttu-id="34974-120">Найден путь.</span><span class="sxs-lookup"><span data-stu-id="34974-120">The path was found.</span></span>
    
 <span data-ttu-id="34974-121">**значения**</span><span class="sxs-lookup"><span data-stu-id="34974-121">**false**</span></span>
  
> <span data-ttu-id="34974-122">Путь не найден.</span><span class="sxs-lookup"><span data-stu-id="34974-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34974-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34974-123">Remarks</span></span>

<span data-ttu-id="34974-124">Используйте функцию **фжеткомпонентпас** , если вам нужно получить путь к закрытой MAPI32. dll.</span><span class="sxs-lookup"><span data-stu-id="34974-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34974-125">См. также</span><span class="sxs-lookup"><span data-stu-id="34974-125">See also</span></span>



[<span data-ttu-id="34974-126">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="34974-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="34974-127">Параметры реестра для заглушки MAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="34974-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

