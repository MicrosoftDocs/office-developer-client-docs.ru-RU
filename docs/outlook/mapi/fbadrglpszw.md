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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808413"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="0ab4f-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="0ab4f-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="0ab4f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ab4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ab4f-105">Проверяет все строки в массив строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="0ab4f-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab4f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0ab4f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ab4f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0ab4f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0ab4f-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0ab4f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ab4f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ab4f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ab4f-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0ab4f-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ab4f-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0ab4f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="0ab4f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ab4f-112">Parameters</span></span>

 <span data-ttu-id="0ab4f-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="0ab4f-113">_lppszW_</span></span>
  
> <span data-ttu-id="0ab4f-114">[in] Указатель на массив строк Юникод, завершающуюся символом null.</span><span class="sxs-lookup"><span data-stu-id="0ab4f-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="0ab4f-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="0ab4f-115">_cStrings_</span></span>
  
> <span data-ttu-id="0ab4f-116">[in] Количество строк в массиве, на который указывает параметр _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="0ab4f-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0ab4f-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0ab4f-117">Return value</span></span>

<span data-ttu-id="0ab4f-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="0ab4f-118">TRUE</span></span> 
  
> <span data-ttu-id="0ab4f-119">Один или несколько строк в указанном массиве являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="0ab4f-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="0ab4f-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ab4f-120">FALSE</span></span> 
  
> <span data-ttu-id="0ab4f-121">Допустимы строки из указанного массива.</span><span class="sxs-lookup"><span data-stu-id="0ab4f-121">The strings in the specified array are valid.</span></span>
    

