---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422280"
---
# <a name="checkparms"></a><span data-ttu-id="7ed13-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="7ed13-103">CheckParms</span></span>

  
  
<span data-ttu-id="7ed13-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed13-105">Вызывает внутреннюю функцию для проверки параметров отладки в методах поставщика услуг, называемых MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ed13-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ed13-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7ed13-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ed13-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7ed13-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7ed13-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7ed13-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7ed13-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed13-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7ed13-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7ed13-110">Called by:</span></span>  <br/> |<span data-ttu-id="7ed13-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="7ed13-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="7ed13-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ed13-112">Parameters</span></span>

 <span data-ttu-id="7ed13-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="7ed13-113">_eMethod_</span></span>
  
> <span data-ttu-id="7ed13-114">[in] Указывает путем переумерия метод проверки.</span><span class="sxs-lookup"><span data-stu-id="7ed13-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="7ed13-115">_First_</span><span class="sxs-lookup"><span data-stu-id="7ed13-115">_First_</span></span>
  
> <span data-ttu-id="7ed13-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="7ed13-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ed13-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ed13-117">Return value</span></span>

<span data-ttu-id="7ed13-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ed13-118">S_OK</span></span> 
  
> <span data-ttu-id="7ed13-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="7ed13-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ed13-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ed13-120">Remarks</span></span>

<span data-ttu-id="7ed13-121">В отличие от макрос [ValidateParms](validateparms.md) и [UlValidateParms](ulvalidateparms.md) макрос, макрос **CheckParms** не выполняет полную проверку параметров.</span><span class="sxs-lookup"><span data-stu-id="7ed13-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="7ed13-122">Параметры, переданные между MAPI и поставщиками услуг, считаются правильными, поэтому **CheckParms** выполняет проверку только отладки.</span><span class="sxs-lookup"><span data-stu-id="7ed13-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

