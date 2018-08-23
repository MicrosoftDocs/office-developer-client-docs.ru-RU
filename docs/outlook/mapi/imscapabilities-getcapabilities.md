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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583276"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="6704d-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="6704d-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="6704d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6704d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6704d-105">Возвращает сведения о хранилище, которое может поддерживать на основании указанного "Выбор".</span><span class="sxs-lookup"><span data-stu-id="6704d-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="6704d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6704d-106">Parameters</span></span>

 <span data-ttu-id="6704d-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="6704d-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="6704d-108">[in] Выбор, определяющее, какие возможности для возврата.</span><span class="sxs-lookup"><span data-stu-id="6704d-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6704d-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6704d-109">Return value</span></span>

<span data-ttu-id="6704d-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="6704d-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="6704d-111">Поддержка для домашних страниц папок в хранилище не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6704d-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="6704d-112">Можно получить, если указано **MSCAP_SEL_FOLDER** в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="6704d-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="6704d-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="6704d-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="6704d-114">Если ограничение содержит все недопустимые аргументы, таких как недопустимые свойства, хранилище игнорирует недопустимых аргументов и обрабатывает только допустимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="6704d-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="6704d-115">Можно получить, если указано **MSCAP_SEL_RESTRICTION** в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="6704d-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="6704d-116">NULL</span><span class="sxs-lookup"><span data-stu-id="6704d-116">NULL</span></span>
  
> <span data-ttu-id="6704d-117">Хранилище не поддерживает все возможности на основании указанного "Выбор".</span><span class="sxs-lookup"><span data-stu-id="6704d-117">The store does not support any capability based on the given selector.</span></span>
    

