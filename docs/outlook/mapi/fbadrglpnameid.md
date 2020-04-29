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
# <a name="fbadrglpnameid"></a><span data-ttu-id="c62c4-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="c62c4-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="c62c4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c62c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c62c4-105">Проверяет массив структур, описывающих именованные свойства, и проверяет их выделение.</span><span class="sxs-lookup"><span data-stu-id="c62c4-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c62c4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c62c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="c62c4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c62c4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c62c4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c62c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c62c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c62c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c62c4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c62c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="c62c4-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c62c4-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="c62c4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c62c4-112">Parameters</span></span>

 <span data-ttu-id="c62c4-113">_лппнамеид_</span><span class="sxs-lookup"><span data-stu-id="c62c4-113">_lppNameId_</span></span>
  
> <span data-ttu-id="c62c4-114">возврата Указатель на массив структур [мапинамеид](mapinameid.md) , описывающих именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c62c4-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="c62c4-115">_записи cName_</span><span class="sxs-lookup"><span data-stu-id="c62c4-115">_cNames_</span></span>
  
> <span data-ttu-id="c62c4-116">возврата Количество именованных структур свойств в массиве, на которое указывает параметр _лппнамеид_ .</span><span class="sxs-lookup"><span data-stu-id="c62c4-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c62c4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c62c4-117">Return value</span></span>

<span data-ttu-id="c62c4-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="c62c4-118">TRUE</span></span> 
  
> <span data-ttu-id="c62c4-119">Одна или несколько указанных структур имени свойства являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="c62c4-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="c62c4-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="c62c4-120">FALSE</span></span> 
  
> <span data-ttu-id="c62c4-121">Указаны допустимые структуры имени свойства.</span><span class="sxs-lookup"><span data-stu-id="c62c4-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c62c4-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c62c4-122">Remarks</span></span>

<span data-ttu-id="c62c4-123">Функцию **фбадрглпнамеид** можно использовать при настройке вызова [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) или [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="c62c4-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

