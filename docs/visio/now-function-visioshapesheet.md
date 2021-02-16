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
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414083"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="abc30-103">NOW Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="abc30-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="abc30-104">Возвращает текущее значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="abc30-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="abc30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abc30-105">Syntax</span></span>

<span data-ttu-id="abc30-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="abc30-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="abc30-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abc30-107">Return value</span></span>

<span data-ttu-id="abc30-108">Дата и время</span><span class="sxs-lookup"><span data-stu-id="abc30-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abc30-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="abc30-109">Remarks</span></span>

<span data-ttu-id="abc30-110">NOW автоматически пересчитываются каждую минуту.</span><span class="sxs-lookup"><span data-stu-id="abc30-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="abc30-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abc30-111">Example 1</span></span>

<span data-ttu-id="abc30-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="abc30-112">NOW( )</span></span>
  
<span data-ttu-id="abc30-113">Возвращает текущую дату и время, например, 27.09.2010 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="abc30-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="abc30-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="abc30-114">Example 2</span></span>

<span data-ttu-id="abc30-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span><span class="sxs-lookup"><span data-stu-id="abc30-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="abc30-116">Возвращает текущую дату и время в формате 27 сентября 2010 г. 12:03.</span><span class="sxs-lookup"><span data-stu-id="abc30-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="abc30-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="abc30-117">Example 3</span></span>

<span data-ttu-id="abc30-118">NOW()+2EW.</span><span class="sxs-lookup"><span data-stu-id="abc30-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="abc30-119">Возвращает текущую дату и время плюс две недели, например 11.01.10, 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="abc30-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

