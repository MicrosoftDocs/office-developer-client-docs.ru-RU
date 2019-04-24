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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328023"
---
# <a name="ftadcft"></a><span data-ttu-id="45f31-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="45f31-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="45f31-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45f31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45f31-105">Добавляет одно целое число без знака 64 в другое, при необходимости используя флаг.</span><span class="sxs-lookup"><span data-stu-id="45f31-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45f31-106">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="45f31-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="45f31-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="45f31-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="45f31-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="45f31-108">Called by:</span></span>  <br/> |<span data-ttu-id="45f31-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="45f31-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="45f31-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f31-110">Parameters</span></span>

 <span data-ttu-id="45f31-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="45f31-111">_ft1_</span></span>
  
> <span data-ttu-id="45f31-112">возврата Структура [fileTime](filetime.md) , содержащая первое 64 – разрядное целое число, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="45f31-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="45f31-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="45f31-113">_ft2_</span></span>
  
> <span data-ttu-id="45f31-114">возврата Структура FILETIME, содержащая второе 64 – разрядное целое число, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="45f31-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="45f31-115">_Пвкарри_</span><span class="sxs-lookup"><span data-stu-id="45f31-115">_pwCarry_</span></span>
  
> <span data-ttu-id="45f31-116">[вход, выход, необязательный] На входе — указатель на флаг входящих данных.</span><span class="sxs-lookup"><span data-stu-id="45f31-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="45f31-117">В выходных данных — указатель на результат сложения.</span><span class="sxs-lookup"><span data-stu-id="45f31-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="45f31-118">Если результат не требуется, этот параметр может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="45f31-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45f31-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45f31-119">Return value</span></span>

<span data-ttu-id="45f31-120">Функция **фтадкфт** возвращает структуру **fileTime** , которая содержит сумму двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="45f31-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="45f31-121">Два входных параметра остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="45f31-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="45f31-122">Если **пвкарри** не имеет значение null, он содержит результат, равный сумме (0 или 1).</span><span class="sxs-lookup"><span data-stu-id="45f31-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="45f31-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45f31-123">Remarks</span></span>

<span data-ttu-id="45f31-124">Функция **фтадкфт** идентична **Фтаддфт** , когда _пвкарри_ имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="45f31-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="45f31-125">Если _пвкарри_ имеет значение, отличное от NULL, а указывает на 0, **фтадкфт** возвращает то же значение **fileTime** , которое возвращает **фтаддфт** .</span><span class="sxs-lookup"><span data-stu-id="45f31-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45f31-126">См. также</span><span class="sxs-lookup"><span data-stu-id="45f31-126">See also</span></span>



[<span data-ttu-id="45f31-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="45f31-127">FtAddFt</span></span>](ftaddft.md)

