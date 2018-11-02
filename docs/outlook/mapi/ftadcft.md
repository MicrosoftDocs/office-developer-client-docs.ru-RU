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
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569773"
---
# <a name="ftadcft"></a><span data-ttu-id="6406d-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="6406d-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="6406d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6406d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6406d-105">Добавляет один целых 64-разрядная версия на другой, при необходимости с помощью реализуемые флаг.</span><span class="sxs-lookup"><span data-stu-id="6406d-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6406d-106">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6406d-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="6406d-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="6406d-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="6406d-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6406d-108">Called by:</span></span>  <br/> |<span data-ttu-id="6406d-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="6406d-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="6406d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6406d-110">Parameters</span></span>

 <span data-ttu-id="6406d-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="6406d-111">_ft1_</span></span>
  
> <span data-ttu-id="6406d-112">[in] Структура [FILETIME](filetime.md) , содержащую первого целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="6406d-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="6406d-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="6406d-113">_ft2_</span></span>
  
> <span data-ttu-id="6406d-114">[in] Структура FILETIME, содержащий второй целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="6406d-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="6406d-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="6406d-115">_pwCarry_</span></span>
  
> <span data-ttu-id="6406d-116">[in, out, необязательно] На входе указатель входящего выполнение флаг.</span><span class="sxs-lookup"><span data-stu-id="6406d-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="6406d-117">На выходе указатель мыши на результат выполнения для добавления.</span><span class="sxs-lookup"><span data-stu-id="6406d-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="6406d-118">Этот параметр может быть NULL, если в результате выполнения не требуется.</span><span class="sxs-lookup"><span data-stu-id="6406d-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6406d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6406d-119">Return value</span></span>

<span data-ttu-id="6406d-120">Функция **FtAdcFt** возвращает структуру **FILETIME** , содержащую сумма двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="6406d-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="6406d-121">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="6406d-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="6406d-122">Если **pwCarry** не равно NULL, в результате выполнения содержит для сумм, 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="6406d-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6406d-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="6406d-123">Remarks</span></span>

<span data-ttu-id="6406d-124">Функция **FtAdcFt** идентична **FtAddFt** при _pwCarry_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="6406d-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="6406d-125">Если _pwCarry_ не равно NULL и указывает на 0, **FtAdcFt** возвращает значение **FILETIME** , которое возвращает **FtAddFt** .</span><span class="sxs-lookup"><span data-stu-id="6406d-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6406d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6406d-126">See also</span></span>



[<span data-ttu-id="6406d-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="6406d-127">FtAddFt</span></span>](ftaddft.md)

