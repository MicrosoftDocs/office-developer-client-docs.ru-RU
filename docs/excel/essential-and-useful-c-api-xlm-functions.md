---
title: Основные и полезные функции XLM API C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [excel 2007], c api xlm
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
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="434c9-104">Основные и полезные функции XLM API C</span><span class="sxs-lookup"><span data-stu-id="434c9-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="434c9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="434c9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="434c9-106">Функции, описанные в этом разделе, — это функции вызова Microsoft Excel, которые особенно полезны разработчикам DLL и XLL.</span><span class="sxs-lookup"><span data-stu-id="434c9-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="434c9-107">Из них функция **xlfRegister** необходима для XLS и DLL, которые хотят зарегистрировать свои функции и команды, чтобы их можно было вызвано непосредственно из Excel.</span><span class="sxs-lookup"><span data-stu-id="434c9-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="434c9-108">Функции **xlfUnregister** и **xlfSetName** используются в сочетании для unregister функций и команд DLL и XLL.</span><span class="sxs-lookup"><span data-stu-id="434c9-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="434c9-109">Excel может использовать множество дополнительных функций с помощью API C, которые полезны при разработке XLL.</span><span class="sxs-lookup"><span data-stu-id="434c9-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="434c9-110">Они соответствуют функциям, функциям и командам листа Excel, которые доступны на листах макроса XLM.</span><span class="sxs-lookup"><span data-stu-id="434c9-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="434c9-111">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="434c9-111">In this section</span></span>

[<span data-ttu-id="434c9-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="434c9-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="434c9-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="434c9-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="434c9-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="434c9-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="434c9-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="434c9-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="434c9-116">xlfRegister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="434c9-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="434c9-117">xlfRegister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="434c9-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="434c9-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="434c9-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="434c9-119">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="434c9-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="434c9-120">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="434c9-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="434c9-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="434c9-121">xlfSetName</span></span>](xlfsetname.md)
  

