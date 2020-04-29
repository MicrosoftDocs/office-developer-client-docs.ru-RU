---
title: Важные и полезная функции функции XLM в C API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [Excel 2007], c API XLM
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434517"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="cfbac-104">Важные и полезная функции функции XLM в C API</span><span class="sxs-lookup"><span data-stu-id="cfbac-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="cfbac-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cfbac-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cfbac-106">Функции, описанные в этом разделе, являются функциями обратного вызова Microsoft Excel, которые особенно удобны для разработчиков DLL и XLL.</span><span class="sxs-lookup"><span data-stu-id="cfbac-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="cfbac-107">В этом случае функция **xlfRegister** важна для XLL-библиотек и библиотек DLL, которые хотят зарегистрировать свои функции и команды, чтобы их можно было вызывать непосредственно из Excel.</span><span class="sxs-lookup"><span data-stu-id="cfbac-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="cfbac-108">Функции **xlfUnregister** и **xlfSetName** используются в сочетании для отмены регистрации DLL и функций XLL и команд.</span><span class="sxs-lookup"><span data-stu-id="cfbac-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="cfbac-109">Многие другие функции Excel предоставляются с помощью API C, которые можно использовать при разработке XLL-модулей.</span><span class="sxs-lookup"><span data-stu-id="cfbac-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="cfbac-110">Они соответствуют функциям и командам листа Excel, которые доступны на листах макросов XLM.</span><span class="sxs-lookup"><span data-stu-id="cfbac-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="cfbac-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="cfbac-111">In this section</span></span>

[<span data-ttu-id="cfbac-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="cfbac-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="cfbac-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="cfbac-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="cfbac-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="cfbac-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="cfbac-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="cfbac-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="cfbac-116">xlfRegister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="cfbac-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="cfbac-117">xlfRegister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="cfbac-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="cfbac-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="cfbac-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="cfbac-119">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="cfbac-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="cfbac-120">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="cfbac-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="cfbac-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="cfbac-121">xlfSetName</span></span>](xlfsetname.md)
  

