---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434832"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="a73ca-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="a73ca-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="a73ca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a73ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a73ca-105">Проверяет массив структур, описывая названные свойства, и проверяет их распределение.</span><span class="sxs-lookup"><span data-stu-id="a73ca-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a73ca-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a73ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="a73ca-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a73ca-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a73ca-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a73ca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a73ca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a73ca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a73ca-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a73ca-110">Called by:</span></span>  <br/> |<span data-ttu-id="a73ca-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a73ca-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="a73ca-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a73ca-112">Parameters</span></span>

 <span data-ttu-id="a73ca-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="a73ca-113">_lppNameId_</span></span>
  
> <span data-ttu-id="a73ca-114">[in] Указатель на массив структур [MAPINAMEID,](mapinameid.md) описывающих названные свойства.</span><span class="sxs-lookup"><span data-stu-id="a73ca-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="a73ca-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="a73ca-115">_cNames_</span></span>
  
> <span data-ttu-id="a73ca-116">[in] Количество именуемой структуры свойств в массиве, на который указывает параметр _lppNameId._</span><span class="sxs-lookup"><span data-stu-id="a73ca-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a73ca-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a73ca-117">Return value</span></span>

<span data-ttu-id="a73ca-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="a73ca-118">TRUE</span></span> 
  
> <span data-ttu-id="a73ca-119">Одна или несколько указанных структур имен свойств недействительны.</span><span class="sxs-lookup"><span data-stu-id="a73ca-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="a73ca-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="a73ca-120">FALSE</span></span> 
  
> <span data-ttu-id="a73ca-121">Указанные структуры имен свойств действительны.</span><span class="sxs-lookup"><span data-stu-id="a73ca-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a73ca-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a73ca-122">Remarks</span></span>

<span data-ttu-id="a73ca-123">Функция **FBadRglpNameID** может использоваться при настройке вызова [в IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="a73ca-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

