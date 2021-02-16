---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160281"
---
# <a name="xleventregister"></a><span data-ttu-id="07ccf-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="07ccf-103">xlEventRegister</span></span>

 <span data-ttu-id="07ccf-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07ccf-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="07ccf-105">Используется для регистрации обработера событий.</span><span class="sxs-lookup"><span data-stu-id="07ccf-105">Used to register an event handler.</span></span> <span data-ttu-id="07ccf-106">Впервые представлена в Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="07ccf-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="07ccf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="07ccf-107">Parameters</span></span>

 <span data-ttu-id="07ccf-108">_pxProcedure_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="07ccf-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="07ccf-109">Имя функции обработера событий, которое отображается в коде DLL.</span><span class="sxs-lookup"><span data-stu-id="07ccf-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="07ccf-110">_pxEvent_ (**xltypeInt)**</span><span class="sxs-lookup"><span data-stu-id="07ccf-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="07ccf-111">Событие, обрабатываемая функцией, указанной в параметре _pxProcedure._</span><span class="sxs-lookup"><span data-stu-id="07ccf-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="07ccf-112">Начиная с Excel 2010, Excel поддерживает следующие события:</span><span class="sxs-lookup"><span data-stu-id="07ccf-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="07ccf-113">**Событие**</span><span class="sxs-lookup"><span data-stu-id="07ccf-113">**Event**</span></span>|<span data-ttu-id="07ccf-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07ccf-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07ccf-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="07ccf-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="07ccf-116">Вызывается, когда Excel завершает вычисление.</span><span class="sxs-lookup"><span data-stu-id="07ccf-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="07ccf-117">После этого события можно освободить все ресурсы, выделенные во время вычисления.</span><span class="sxs-lookup"><span data-stu-id="07ccf-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="07ccf-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="07ccf-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="07ccf-119">Вызывается, когда пользователь прерывает вычисление.</span><span class="sxs-lookup"><span data-stu-id="07ccf-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="07ccf-120">XLL должна останавливать любые асинхронные действия.</span><span class="sxs-lookup"><span data-stu-id="07ccf-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="07ccf-121">Событие CalculationEnded вызывается сразу после этого события.</span><span class="sxs-lookup"><span data-stu-id="07ccf-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="07ccf-122">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07ccf-122">Property value/Return value</span></span>

<span data-ttu-id="07ccf-123">В случае успеха pxRes (**xltypeInt)** имеет значение > 0.</span><span class="sxs-lookup"><span data-stu-id="07ccf-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="07ccf-124">Если не удалось, pxRes ==0.</span><span class="sxs-lookup"><span data-stu-id="07ccf-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07ccf-125">См. также</span><span class="sxs-lookup"><span data-stu-id="07ccf-125">See also</span></span>



[<span data-ttu-id="07ccf-126">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="07ccf-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

