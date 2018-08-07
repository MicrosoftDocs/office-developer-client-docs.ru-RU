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
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808515"
---
# <a name="ftadcft"></a><span data-ttu-id="bc05c-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="bc05c-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="bc05c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc05c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc05c-105">Добавляет один целых 64-разрядная версия на другой, при необходимости с помощью реализуемые флаг.</span><span class="sxs-lookup"><span data-stu-id="bc05c-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc05c-106">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="bc05c-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc05c-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc05c-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc05c-108">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="bc05c-108">Called by:</span></span>  <br/> |<span data-ttu-id="bc05c-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="bc05c-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="bc05c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc05c-110">Parameters</span></span>

 <span data-ttu-id="bc05c-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="bc05c-111">_ft1_</span></span>
  
> <span data-ttu-id="bc05c-112">[in] Структура [FILETIME](filetime.md) , содержащую первого целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="bc05c-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="bc05c-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="bc05c-113">_ft2_</span></span>
  
> <span data-ttu-id="bc05c-114">[in] Структура FILETIME, содержащий второй целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="bc05c-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="bc05c-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="bc05c-115">_pwCarry_</span></span>
  
> <span data-ttu-id="bc05c-116">[in, out, необязательно] На входе указатель входящего выполнение флаг.</span><span class="sxs-lookup"><span data-stu-id="bc05c-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="bc05c-117">На выходе указатель мыши на результат выполнения для добавления.</span><span class="sxs-lookup"><span data-stu-id="bc05c-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="bc05c-118">Этот параметр может быть NULL, если в результате выполнения не требуется.</span><span class="sxs-lookup"><span data-stu-id="bc05c-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc05c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="bc05c-120">Функция **FtAdcFt** возвращает структуру **FILETIME** , содержащую сумма двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="bc05c-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="bc05c-121">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="bc05c-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="bc05c-122">Если **pwCarry** не равно NULL, в результате выполнения содержит для сумм, 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="bc05c-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc05c-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc05c-123">Remarks</span></span>

<span data-ttu-id="bc05c-124">Функция **FtAdcFt** идентична **FtAddFt** при _pwCarry_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bc05c-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="bc05c-125">Если _pwCarry_ не равно NULL и указывает на 0, **FtAdcFt** возвращает значение **FILETIME** , которое возвращает **FtAddFt** .</span><span class="sxs-lookup"><span data-stu-id="bc05c-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc05c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bc05c-126">See also</span></span>



[<span data-ttu-id="bc05c-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="bc05c-127">FtAddFt</span></span>](ftaddft.md)

