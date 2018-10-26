---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565916"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="06d1f-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="06d1f-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="06d1f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06d1f-105">Проверяет все строки в массив строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="06d1f-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06d1f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="06d1f-106">Header file:</span></span>  <br/> |<span data-ttu-id="06d1f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="06d1f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="06d1f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="06d1f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="06d1f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="06d1f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="06d1f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="06d1f-110">Called by:</span></span>  <br/> |<span data-ttu-id="06d1f-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="06d1f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="06d1f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="06d1f-112">Parameters</span></span>

 <span data-ttu-id="06d1f-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="06d1f-113">_lppszW_</span></span>
  
> <span data-ttu-id="06d1f-114">[in] Указатель на массив строк Юникод, завершающуюся символом null.</span><span class="sxs-lookup"><span data-stu-id="06d1f-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="06d1f-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="06d1f-115">_cStrings_</span></span>
  
> <span data-ttu-id="06d1f-116">[in] Количество строк в массиве, на который указывает параметр _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="06d1f-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="06d1f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06d1f-117">Return value</span></span>

<span data-ttu-id="06d1f-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="06d1f-118">TRUE</span></span> 
  
> <span data-ttu-id="06d1f-119">Один или несколько строк в указанном массиве являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="06d1f-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="06d1f-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="06d1f-120">FALSE</span></span> 
  
> <span data-ttu-id="06d1f-121">Допустимы строки из указанного массива.</span><span class="sxs-lookup"><span data-stu-id="06d1f-121">The strings in the specified array are valid.</span></span>
    

