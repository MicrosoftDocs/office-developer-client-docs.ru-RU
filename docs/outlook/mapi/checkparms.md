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
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808168"
---
# <a name="checkparms"></a><span data-ttu-id="b2ba8-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="b2ba8-103">CheckParms</span></span>

  
  
<span data-ttu-id="b2ba8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2ba8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2ba8-105">Вызывает внутренней функции для проверки параметров отладки на методы поставщика службы вызывается MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2ba8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b2ba8-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2ba8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b2ba8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b2ba8-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b2ba8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b2ba8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b2ba8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b2ba8-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b2ba8-110">Called by:</span></span>  <br/> |<span data-ttu-id="b2ba8-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b2ba8-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b2ba8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2ba8-112">Parameters</span></span>

 <span data-ttu-id="b2ba8-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="b2ba8-113">_eMethod_</span></span>
  
> <span data-ttu-id="b2ba8-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b2ba8-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="b2ba8-115">_First_</span></span>
  
> <span data-ttu-id="b2ba8-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2ba8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="b2ba8-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b2ba8-118">S_OK</span></span> 
  
> <span data-ttu-id="b2ba8-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2ba8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2ba8-120">Remarks</span></span>

<span data-ttu-id="b2ba8-121">В отличие от макросы [ValidateParms](validateparms.md) и [UlValidateParms](ulvalidateparms.md) **CheckParms** макрос не выполняет проверку параметров.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="b2ba8-122">Параметры, переданные между MAPI и службой поставщиков считаются правильно, поэтому **CheckParms** выполняет только проверку отладки.</span><span class="sxs-lookup"><span data-stu-id="b2ba8-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

