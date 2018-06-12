---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807352"
---
# <a name="xleventregister"></a><span data-ttu-id="91fd9-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="91fd9-103">xlEventRegister</span></span>

 <span data-ttu-id="91fd9-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="91fd9-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="91fd9-105">Используется для регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="91fd9-105">Used to register an event handler.</span></span> <span data-ttu-id="91fd9-106">Появился в Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="91fd9-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="91fd9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="91fd9-107">Parameters</span></span>

 <span data-ttu-id="91fd9-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="91fd9-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="91fd9-109">Имя функции обработчика событий как оно отображается в коде DLL.</span><span class="sxs-lookup"><span data-stu-id="91fd9-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="91fd9-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="91fd9-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="91fd9-111">Событие обрабатывается с помощью функции, указанный в параметре _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="91fd9-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="91fd9-112">Начиная с версии Excel 2010, Excel поддерживает следующие события:</span><span class="sxs-lookup"><span data-stu-id="91fd9-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="91fd9-113">**Событие**</span><span class="sxs-lookup"><span data-stu-id="91fd9-113">**Event**</span></span>|<span data-ttu-id="91fd9-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91fd9-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91fd9-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="91fd9-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="91fd9-116">Возникает после завершения вычислений Excel.</span><span class="sxs-lookup"><span data-stu-id="91fd9-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="91fd9-117">Можно освободить все ресурсы, выделенные при расчете после этого события.</span><span class="sxs-lookup"><span data-stu-id="91fd9-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="91fd9-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="91fd9-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="91fd9-119">Возникает, когда пользователь прерывает вычисления.</span><span class="sxs-lookup"><span data-stu-id="91fd9-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="91fd9-120">XLL необходимо остановить любые асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="91fd9-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="91fd9-121">Событие CalculationEnded вызывается сразу после этого события.</span><span class="sxs-lookup"><span data-stu-id="91fd9-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="91fd9-122">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91fd9-122">Property value/Return value</span></span>

<span data-ttu-id="91fd9-123">В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="91fd9-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="91fd9-124">В случае неудачи возвращает **значение FALSE**.</span><span class="sxs-lookup"><span data-stu-id="91fd9-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91fd9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="91fd9-125">See also</span></span>



[<span data-ttu-id="91fd9-126">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="91fd9-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

