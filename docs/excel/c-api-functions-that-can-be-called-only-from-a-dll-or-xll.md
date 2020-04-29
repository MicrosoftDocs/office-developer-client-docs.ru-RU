---
title: Функции API C, которые можно вызывать только из библиотеки DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [Excel 2007], API c, вызванные из DLL или XLL
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423120"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="3b134-104">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="3b134-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="3b134-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b134-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3b134-106">API C предоставляет 15 функций обратного вызова Microsoft Excel, которые можно вызывать только с помощью функций **Excel4**, **Excel4v**, **Excel12**или **Excel12v** (или с помощью одной из этих функций, косвенно с помощью функции **Excel** или **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="3b134-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="3b134-107">Это означает, что они могут вызываться только из библиотеки DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="3b134-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3b134-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3b134-108">In this section</span></span>

[<span data-ttu-id="3b134-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="3b134-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="3b134-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="3b134-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="3b134-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="3b134-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="3b134-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="3b134-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="3b134-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="3b134-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="3b134-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="3b134-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="3b134-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="3b134-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="3b134-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="3b134-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="3b134-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="3b134-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="3b134-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="3b134-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="3b134-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="3b134-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="3b134-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="3b134-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="3b134-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="3b134-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="3b134-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="3b134-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="3b134-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="3b134-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="3b134-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="3b134-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="3b134-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="3b134-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="3b134-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="3b134-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="3b134-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="3b134-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="3b134-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3b134-128">See also</span></span>



[<span data-ttu-id="3b134-129">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="3b134-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

