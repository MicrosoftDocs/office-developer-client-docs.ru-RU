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
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436442"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="b2b25-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="b2b25-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="b2b25-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2b25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2b25-105">Проверяет все строки в массиве строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="b2b25-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2b25-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b2b25-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2b25-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b2b25-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b2b25-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b2b25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b2b25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b2b25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b2b25-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b2b25-110">Called by:</span></span>  <br/> |<span data-ttu-id="b2b25-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b2b25-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="b2b25-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2b25-112">Parameters</span></span>

 <span data-ttu-id="b2b25-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="b2b25-113">_lppszW_</span></span>
  
> <span data-ttu-id="b2b25-114">[in] Указатель на массив строк Юникода, осекаемого нулью.</span><span class="sxs-lookup"><span data-stu-id="b2b25-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="b2b25-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="b2b25-115">_cStrings_</span></span>
  
> <span data-ttu-id="b2b25-116">[in] Количество строк в массиве, на которые указывает параметр _lppszW._</span><span class="sxs-lookup"><span data-stu-id="b2b25-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2b25-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2b25-117">Return value</span></span>

<span data-ttu-id="b2b25-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2b25-118">TRUE</span></span> 
  
> <span data-ttu-id="b2b25-119">Одна или несколько строк в указанном массиве являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="b2b25-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="b2b25-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2b25-120">FALSE</span></span> 
  
> <span data-ttu-id="b2b25-121">Строки в указанном массиве допустимы.</span><span class="sxs-lookup"><span data-stu-id="b2b25-121">The strings in the specified array are valid.</span></span>
    

