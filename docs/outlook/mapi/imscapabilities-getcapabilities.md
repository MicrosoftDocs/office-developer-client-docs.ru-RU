---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809363"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="c1437-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c1437-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="c1437-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1437-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1437-105">Возвращает сведения о хранилище, которое может поддерживать на основании указанного "Выбор".</span><span class="sxs-lookup"><span data-stu-id="c1437-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="c1437-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1437-106">Parameters</span></span>

 <span data-ttu-id="c1437-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="c1437-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="c1437-108">[in] Выбор, определяющее, какие возможности для возврата.</span><span class="sxs-lookup"><span data-stu-id="c1437-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1437-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="c1437-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="c1437-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="c1437-111">Поддержка для домашних страниц папок в хранилище не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1437-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="c1437-112">Можно получить, если указано **MSCAP_SEL_FOLDER** в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="c1437-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="c1437-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="c1437-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="c1437-114">Если ограничение содержит все недопустимые аргументы, таких как недопустимые свойства, хранилище игнорирует недопустимых аргументов и обрабатывает только допустимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="c1437-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="c1437-115">Можно получить, если указано **MSCAP_SEL_RESTRICTION** в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="c1437-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="c1437-116">NULL</span><span class="sxs-lookup"><span data-stu-id="c1437-116">NULL</span></span>
  
> <span data-ttu-id="c1437-117">Хранилище не поддерживает все возможности на основании указанного "Выбор".</span><span class="sxs-lookup"><span data-stu-id="c1437-117">The store does not support any capability based on the given selector.</span></span>
    

