---
title: Функции API C, которые можно вызывать только из библиотеки DLL или XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [excel 2007], c api вызов выполняется из dll или xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807151"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="6d853-104">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="6d853-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="6d853-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d853-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6d853-106">API-Интерфейс C предоставляет 15 функции обратного вызова Microsoft Excel, которые могут вызываться только с помощью **Excel4**, **Excel4v**, **Excel12**или **Excel12v** функции (или один из этих функций, косвенно с помощью функции Framework **Excel **или **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="6d853-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="6d853-107">Это означает, что они могут вызываться только из DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="6d853-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="6d853-108">В этой статье</span><span class="sxs-lookup"><span data-stu-id="6d853-108">In this section</span></span>

[<span data-ttu-id="6d853-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="6d853-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="6d853-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="6d853-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="6d853-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="6d853-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="6d853-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="6d853-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="6d853-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="6d853-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="6d853-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="6d853-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="6d853-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="6d853-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="6d853-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="6d853-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="6d853-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="6d853-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="6d853-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="6d853-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="6d853-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="6d853-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="6d853-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="6d853-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="6d853-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="6d853-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="6d853-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="6d853-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="6d853-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="6d853-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="6d853-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="6d853-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="6d853-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="6d853-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="6d853-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="6d853-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="6d853-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="6d853-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="6d853-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6d853-128">See also</span></span>



[<span data-ttu-id="6d853-129">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="6d853-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

