---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Возвращает текущее значение даты и времени.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814331"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="5b963-103">NOW Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5b963-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5b963-104">Возвращает текущее значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5b963-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5b963-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b963-105">Syntax</span></span>

<span data-ttu-id="5b963-106">ТЕПЕРЬ)</span><span class="sxs-lookup"><span data-stu-id="5b963-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="5b963-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="5b963-108">Даты и времени</span><span class="sxs-lookup"><span data-stu-id="5b963-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b963-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="5b963-109">Remarks</span></span>

<span data-ttu-id="5b963-110">ТЕПЕРЬ автоматически пересчитывается каждую минуту.</span><span class="sxs-lookup"><span data-stu-id="5b963-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5b963-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b963-111">Example 1</span></span>

<span data-ttu-id="5b963-112">ТЕПЕРЬ)</span><span class="sxs-lookup"><span data-stu-id="5b963-112">NOW( )</span></span>
  
<span data-ttu-id="5b963-113">Возвращает текущую дату и время, например 9/27/2010 12:03:30 PM.</span><span class="sxs-lookup"><span data-stu-id="5b963-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5b963-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5b963-114">Example 2</span></span>

<span data-ttu-id="5b963-115">ФОРМАТ (СЕЙЧАС (), «ДД МММ. гггг чч: мм»)</span><span class="sxs-lookup"><span data-stu-id="5b963-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="5b963-116">Возвращает текущую дату и время в формате 27 сентября 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="5b963-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5b963-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5b963-117">Example 3</span></span>

<span data-ttu-id="5b963-118">ТЕПЕРЬ () + 2EW.</span><span class="sxs-lookup"><span data-stu-id="5b963-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="5b963-119">Возвращает текущую дату и время плюс две недели затраченное, например, 10 и 11/10 12:03:30 PM.</span><span class="sxs-lookup"><span data-stu-id="5b963-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

