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
# <a name="ftadcft"></a><span data-ttu-id="e1886-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="e1886-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="e1886-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1886-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1886-105">Добавляет одно неподписаное 64-битное 64-битное другое, при желании с помощью флага переноса.</span><span class="sxs-lookup"><span data-stu-id="e1886-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1886-106">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e1886-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1886-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1886-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1886-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e1886-108">Called by:</span></span>  <br/> |<span data-ttu-id="e1886-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="e1886-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="e1886-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1886-110">Parameters</span></span>

 <span data-ttu-id="e1886-111">_ft1_</span><span class="sxs-lookup"><span data-stu-id="e1886-111">_ft1_</span></span>
  
> <span data-ttu-id="e1886-112">[in] Структура [FILETIME,](filetime.md) которая содержит первое неподписаное 64-битное количество, которое необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="e1886-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="e1886-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="e1886-113">_ft2_</span></span>
  
> <span data-ttu-id="e1886-114">[in] Структура FILETIME, которая содержит второе 64-битное неподписаенное 64-битное, которое необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="e1886-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="e1886-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="e1886-115">_pwCarry_</span></span>
  
> <span data-ttu-id="e1886-116">[in, out, optional] При вводе указатель на входящий флаг переноса.</span><span class="sxs-lookup"><span data-stu-id="e1886-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="e1886-117">При выходе указатель на результат переноса для добавления.</span><span class="sxs-lookup"><span data-stu-id="e1886-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="e1886-118">Этот параметр может иметь NULL, если результат переноса не требуется.</span><span class="sxs-lookup"><span data-stu-id="e1886-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1886-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1886-119">Return value</span></span>

<span data-ttu-id="e1886-120">Функция **FtAdcFt** возвращает структуру **FILETIME,** которая содержит сумму двух integers.</span><span class="sxs-lookup"><span data-stu-id="e1886-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="e1886-121">Два входных параметра остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="e1886-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="e1886-122">Если **pwCarry** не имеет NULL, он содержит результат переноса для суммы, 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="e1886-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e1886-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1886-123">Remarks</span></span>

<span data-ttu-id="e1886-124">Функция **FtAdcFt** идентична **функции FtAddFt,**  _если pwCarry_ имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="e1886-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="e1886-125">Если _pwCarry не_ имеет значение NULL и указывает на 0, **FtAdcFt** возвращает то же **значение FILETIME,** что **и FtAddFt.**</span><span class="sxs-lookup"><span data-stu-id="e1886-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1886-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e1886-126">See also</span></span>



[<span data-ttu-id="e1886-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="e1886-127">FtAddFt</span></span>](ftaddft.md)

