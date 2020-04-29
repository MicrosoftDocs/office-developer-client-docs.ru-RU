---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438766"
---
# <a name="xleventregister"></a><span data-ttu-id="82bf1-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="82bf1-103">xlEventRegister</span></span>

 <span data-ttu-id="82bf1-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82bf1-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82bf1-105">Используется для регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="82bf1-105">Used to register an event handler.</span></span> <span data-ttu-id="82bf1-106">Представлены в Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="82bf1-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="82bf1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="82bf1-107">Parameters</span></span>

 <span data-ttu-id="82bf1-108">_пкспроцедуре_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="82bf1-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="82bf1-109">Имя функции обработчика событий в том виде, в котором оно отображается в коде DLL.</span><span class="sxs-lookup"><span data-stu-id="82bf1-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="82bf1-110">_пксевент_ (**кслтипеинт**)</span><span class="sxs-lookup"><span data-stu-id="82bf1-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="82bf1-111">Событие, обрабатываемое функцией, указанной в параметре _пкспроцедуре_ .</span><span class="sxs-lookup"><span data-stu-id="82bf1-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="82bf1-112">Начиная с Excel 2010, Excel поддерживает следующие события:</span><span class="sxs-lookup"><span data-stu-id="82bf1-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="82bf1-113">**Event**</span><span class="sxs-lookup"><span data-stu-id="82bf1-113">**Event**</span></span>|<span data-ttu-id="82bf1-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="82bf1-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82bf1-115">**кслевенткалкулатионендед**</span><span class="sxs-lookup"><span data-stu-id="82bf1-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="82bf1-116">Создается, когда Excel завершает вычисление.</span><span class="sxs-lookup"><span data-stu-id="82bf1-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="82bf1-117">После этого события можно освобождать ресурсы, выделенные в ходе вычисления.</span><span class="sxs-lookup"><span data-stu-id="82bf1-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="82bf1-118">**кслевенткалкулатионканцелед**</span><span class="sxs-lookup"><span data-stu-id="82bf1-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="82bf1-119">Создается, когда пользователь прерывает вычисление.</span><span class="sxs-lookup"><span data-stu-id="82bf1-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="82bf1-120">XLL должен остановить все асинхронные действия.</span><span class="sxs-lookup"><span data-stu-id="82bf1-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="82bf1-121">Событие Калкулатионендед вызывается сразу после этого события.</span><span class="sxs-lookup"><span data-stu-id="82bf1-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="82bf1-122">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82bf1-122">Property value/Return value</span></span>

<span data-ttu-id="82bf1-123">В случае успеха возвращает **значение true** (**кслтипебул**).</span><span class="sxs-lookup"><span data-stu-id="82bf1-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="82bf1-124">В случае неудачной попытки возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="82bf1-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82bf1-125">См. также</span><span class="sxs-lookup"><span data-stu-id="82bf1-125">See also</span></span>



[<span data-ttu-id="82bf1-126">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="82bf1-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

