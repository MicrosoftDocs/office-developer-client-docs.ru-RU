---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812284"
---
# <a name="sizedadrlist"></a><span data-ttu-id="de2ea-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="de2ea-103">SizedADRLIST</span></span>

<span data-ttu-id="de2ea-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de2ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de2ea-105">Определяет структуру [ADRLIST](adrlist.md) с указанным именем, содержащий указанное число [ADRENTRY](adrentry.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="de2ea-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de2ea-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="de2ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="de2ea-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de2ea-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de2ea-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="de2ea-108">Related structure:</span></span>  <br/> |<span data-ttu-id="de2ea-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="de2ea-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="de2ea-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="de2ea-110">Parameters</span></span>

<span data-ttu-id="de2ea-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="de2ea-111">__centries_</span></span>
  
> <span data-ttu-id="de2ea-112">Число структур **ADRENTRY** должны быть включены в новой структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="de2ea-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="de2ea-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="de2ea-113">__name_</span></span>
  
> <span data-ttu-id="de2ea-114">Имя для новой структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="de2ea-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de2ea-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="de2ea-115">Remarks</span></span>

<span data-ttu-id="de2ea-116">Макрос **SizedADRLIST** позволяет определить список получателей, который имеет явные границы, когда известны требования к длине массива.</span><span class="sxs-lookup"><span data-stu-id="de2ea-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="de2ea-117">Приведенный ниже код показано, как приведения результатов макроса **SizedADRLIST** в структуре указатель **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="de2ea-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="de2ea-118">См. также</span><span class="sxs-lookup"><span data-stu-id="de2ea-118">See also</span></span>

- [<span data-ttu-id="de2ea-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="de2ea-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="de2ea-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="de2ea-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="de2ea-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="de2ea-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

