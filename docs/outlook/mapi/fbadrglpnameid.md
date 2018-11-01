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
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588148"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="98e4d-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="98e4d-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="98e4d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98e4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98e4d-105">Проверяет массив структур, которые описывают с именем свойства и проверяет их выделении.</span><span class="sxs-lookup"><span data-stu-id="98e4d-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98e4d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="98e4d-106">Header file:</span></span>  <br/> |<span data-ttu-id="98e4d-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="98e4d-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="98e4d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="98e4d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98e4d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98e4d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98e4d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="98e4d-110">Called by:</span></span>  <br/> |<span data-ttu-id="98e4d-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="98e4d-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="98e4d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="98e4d-112">Parameters</span></span>

 <span data-ttu-id="98e4d-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="98e4d-113">_lppNameId_</span></span>
  
> <span data-ttu-id="98e4d-114">[in] Указатель на массив структур [MAPINAMEID](mapinameid.md) , описывающее именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="98e4d-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="98e4d-115">_записи CNAME_</span><span class="sxs-lookup"><span data-stu-id="98e4d-115">_cNames_</span></span>
  
> <span data-ttu-id="98e4d-116">[in] Число структур именованное свойство в массиве указывает параметр _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="98e4d-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98e4d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e4d-117">Return value</span></span>

<span data-ttu-id="98e4d-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="98e4d-118">TRUE</span></span> 
  
> <span data-ttu-id="98e4d-119">Один или несколько структур имя указанного свойства является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="98e4d-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="98e4d-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="98e4d-120">FALSE</span></span> 
  
> <span data-ttu-id="98e4d-121">Структуры имя указанного свойства являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="98e4d-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98e4d-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="98e4d-122">Remarks</span></span>

<span data-ttu-id="98e4d-123">Функция **FBadRglpNameID** можно использовать при настройке для вызова [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="98e4d-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

