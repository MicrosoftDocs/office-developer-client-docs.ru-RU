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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331803"
---
# <a name="checkparms"></a><span data-ttu-id="ccdcc-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="ccdcc-103">CheckParms</span></span>

  
  
<span data-ttu-id="ccdcc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccdcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccdcc-105">Вызывает внутреннюю функцию для проверки параметров отладки методов поставщика услуг, вызываемых MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccdcc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ccdcc-106">Header file:</span></span>  <br/> |<span data-ttu-id="ccdcc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ccdcc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ccdcc-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ccdcc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ccdcc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ccdcc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ccdcc-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ccdcc-110">Called by:</span></span>  <br/> |<span data-ttu-id="ccdcc-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ccdcc-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="ccdcc-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccdcc-112">Parameters</span></span>

 <span data-ttu-id="ccdcc-113">_Емесод_</span><span class="sxs-lookup"><span data-stu-id="ccdcc-113">_eMethod_</span></span>
  
> <span data-ttu-id="ccdcc-114">возврата Определяет, по перечислению, метод, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="ccdcc-115">_First_</span><span class="sxs-lookup"><span data-stu-id="ccdcc-115">_First_</span></span>
  
> <span data-ttu-id="ccdcc-116">возврата Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccdcc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccdcc-117">Return value</span></span>

<span data-ttu-id="ccdcc-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccdcc-118">S_OK</span></span> 
  
> <span data-ttu-id="ccdcc-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccdcc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccdcc-120">Remarks</span></span>

<span data-ttu-id="ccdcc-121">В отличие от макросов [валидатепармс](validateparms.md) и [Улвалидатепармс](ulvalidateparms.md) , макрос **чеккпармс** не выполняет полную проверку параметров.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="ccdcc-122">Параметры, передаваемые между MAPI и поставщиками услуг, считаются правильными, поэтому **чеккпармс** выполняет только проверку отладки.</span><span class="sxs-lookup"><span data-stu-id="ccdcc-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

