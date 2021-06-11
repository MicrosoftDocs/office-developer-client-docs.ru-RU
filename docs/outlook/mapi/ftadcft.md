---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429707"
---
# <a name="ftadcft"></a><span data-ttu-id="02061-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="02061-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="02061-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02061-105">Добавляет один неподписаный 64-битный пакет в другой, необязательно с помощью флага переноса.</span><span class="sxs-lookup"><span data-stu-id="02061-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02061-106">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="02061-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="02061-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="02061-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="02061-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="02061-108">Called by:</span></span>  <br/> |<span data-ttu-id="02061-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="02061-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="02061-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="02061-110">Parameters</span></span>

 <span data-ttu-id="02061-111">_ft1_</span><span class="sxs-lookup"><span data-stu-id="02061-111">_ft1_</span></span>
  
> <span data-ttu-id="02061-112">[in] Структура [FILETIME,](filetime.md) которая содержит первый неподписаный 64-битный набор, который будет добавлен.</span><span class="sxs-lookup"><span data-stu-id="02061-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="02061-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="02061-113">_ft2_</span></span>
  
> <span data-ttu-id="02061-114">[in] Структура FILETIME, которая содержит вторую неподписаную 64-битную 64-битную структуру, которая будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="02061-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="02061-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="02061-115">_pwCarry_</span></span>
  
> <span data-ttu-id="02061-116">[in, out, необязательный] На входе указатель на входящий флаг переноса.</span><span class="sxs-lookup"><span data-stu-id="02061-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="02061-117">На выходе указатель на результат переноса для добавления.</span><span class="sxs-lookup"><span data-stu-id="02061-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="02061-118">Этот параметр может быть NULL, если результат переноса не требуется.</span><span class="sxs-lookup"><span data-stu-id="02061-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02061-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02061-119">Return value</span></span>

<span data-ttu-id="02061-120">Функция **FtAdcFt** возвращает структуру **FILETIME,** которая содержит сумму двух integers.</span><span class="sxs-lookup"><span data-stu-id="02061-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="02061-121">Два параметра ввода остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="02061-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="02061-122">Если **pwCarry не** является NULL, он содержит результат переноса для суммы 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="02061-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02061-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="02061-123">Remarks</span></span>

<span data-ttu-id="02061-124">Функция **FtAdcFt** идентична **функции FtAddFt,** когда  _pwCarry_ является NULL.</span><span class="sxs-lookup"><span data-stu-id="02061-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="02061-125">Если _pwCarry не_ является NULL и указывает на значение 0, **FtAdcFt** возвращает то же значение **FILETIME,** которое **возвращает FtAddFt.**</span><span class="sxs-lookup"><span data-stu-id="02061-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02061-126">См. также</span><span class="sxs-lookup"><span data-stu-id="02061-126">See also</span></span>



[<span data-ttu-id="02061-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="02061-127">FtAddFt</span></span>](ftaddft.md)

