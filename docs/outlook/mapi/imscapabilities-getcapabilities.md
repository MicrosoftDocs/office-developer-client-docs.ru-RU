---
title: имскапабилитиесжеткапабилитиес
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
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409260"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="4d86b-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="4d86b-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="4d86b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d86b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d86b-105">Получает сведения о том, что хранилище может поддерживаться в соответствии с указанным селектором.</span><span class="sxs-lookup"><span data-stu-id="4d86b-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="4d86b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d86b-106">Parameters</span></span>

 <span data-ttu-id="4d86b-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="4d86b-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="4d86b-108">возврата Селектор, указывающий, какие возможности следует возвращать.</span><span class="sxs-lookup"><span data-stu-id="4d86b-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d86b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d86b-109">Return value</span></span>

<span data-ttu-id="4d86b-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="4d86b-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="4d86b-111">Поддержка домашних страниц папок в хранилище, не являющемся хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d86b-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="4d86b-112">Это может быть возвращено, если **MSCAP_SEL_FOLDER** указан в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="4d86b-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="4d86b-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="4d86b-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="4d86b-114">Если ограничение содержит любые недопустимые аргументы, такие как недопустимые свойства, хранилище игнорирует недопустимые аргументы и обрабатывает только допустимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="4d86b-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="4d86b-115">Это может быть возвращено, если **MSCAP_SEL_RESTRICTION** указан в *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="4d86b-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="4d86b-116">ОПРЕДЕЛЕН</span><span class="sxs-lookup"><span data-stu-id="4d86b-116">NULL</span></span>
  
> <span data-ttu-id="4d86b-117">Хранилище не поддерживает никакие возможности на основе данного селектора.</span><span class="sxs-lookup"><span data-stu-id="4d86b-117">The store does not support any capability based on the given selector.</span></span>
    

