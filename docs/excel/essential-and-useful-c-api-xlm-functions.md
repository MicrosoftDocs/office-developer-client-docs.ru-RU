---
title: Важные и полезная функции функции XLM В C API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [Excel 2007], c API XLM
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311125"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="b2af5-104">Важные и полезная функции функции XLM В C API</span><span class="sxs-lookup"><span data-stu-id="b2af5-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="b2af5-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2af5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b2af5-106">Функции, описанные в этом разделе, являются функциями обратного вызова Microsoft Excel, которые особенно удобны для разработчиков DLL и XLL.</span><span class="sxs-lookup"><span data-stu-id="b2af5-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="b2af5-107">В этом случае функция **xlfRegister** важна для XLL-библиотек и библиотек DLL, которые хотят зарегистрировать свои функции и команды, чтобы их можно было вызывать непосредственно из Excel.</span><span class="sxs-lookup"><span data-stu-id="b2af5-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="b2af5-108">Функции **xlfUnregister** и **xlfSetName** используются в сочетании для отмены регистрации DLL и функций XLL и команд.</span><span class="sxs-lookup"><span data-stu-id="b2af5-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="b2af5-109">Многие другие функции Excel предоставляются с помощью API C, которые можно использовать при разработке XLL-модулей.</span><span class="sxs-lookup"><span data-stu-id="b2af5-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="b2af5-110">Они соответствуют функциям и командам листа Excel, которые доступны на листах макросов XLM.</span><span class="sxs-lookup"><span data-stu-id="b2af5-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b2af5-111">Содержание</span><span class="sxs-lookup"><span data-stu-id="b2af5-111">In this section</span></span>

[<span data-ttu-id="b2af5-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="b2af5-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="b2af5-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="b2af5-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="b2af5-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="b2af5-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="b2af5-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="b2af5-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="b2af5-116">xlfRegister (����� 1)</span><span class="sxs-lookup"><span data-stu-id="b2af5-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="b2af5-117">xlfRegister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="b2af5-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="b2af5-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="b2af5-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="b2af5-119">xlfUnregister (форма 1)</span><span class="sxs-lookup"><span data-stu-id="b2af5-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="b2af5-120">xlfUnregister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="b2af5-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="b2af5-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="b2af5-121">xlfSetName</span></span>](xlfsetname.md)
  

