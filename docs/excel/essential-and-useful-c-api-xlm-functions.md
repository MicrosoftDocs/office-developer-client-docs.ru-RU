---
title: Функции API XLM важные и полезные C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807170"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="65353-104">Функции API XLM важные и полезные C</span><span class="sxs-lookup"><span data-stu-id="65353-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="65353-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="65353-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="65353-106">Функции, описанных в данном разделе, функции обратного вызова Microsoft Excel, которые особенно полезны для разработчиков, DLL-Библиотеку и XLL.</span><span class="sxs-lookup"><span data-stu-id="65353-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="65353-107">Эти функция **xlfRegister** необходима для XLL-модулей и библиотеки DLL, которые нужно зарегистрировать их функции и команды, чтобы они могут вызываться непосредственно из Excel.</span><span class="sxs-lookup"><span data-stu-id="65353-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="65353-108">Функции **xlfUnregister** и **xlfSetName** используются в сочетании для отмены регистрации DLL-Библиотеку и XLL функций и команд.</span><span class="sxs-lookup"><span data-stu-id="65353-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="65353-109">Много новых функций, предоставляемых Excel с помощью интерфейса API для C, полезные при разработке XLL-модулей.</span><span class="sxs-lookup"><span data-stu-id="65353-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="65353-110">Они соответствуют листа Excel функции и функции и команды, которые доступны из листы макросов XLM.</span><span class="sxs-lookup"><span data-stu-id="65353-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="65353-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="65353-111">In this section</span></span>

[<span data-ttu-id="65353-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="65353-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="65353-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="65353-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="65353-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="65353-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="65353-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="65353-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="65353-116">xlfRegister (����� 1)</span><span class="sxs-lookup"><span data-stu-id="65353-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="65353-117">xlfRegister (формы 2)</span><span class="sxs-lookup"><span data-stu-id="65353-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="65353-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="65353-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="65353-119">xlfUnregister (формы 1)</span><span class="sxs-lookup"><span data-stu-id="65353-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="65353-120">xlfUnregister (формы 2)</span><span class="sxs-lookup"><span data-stu-id="65353-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="65353-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="65353-121">xlfSetName</span></span>](xlfsetname.md)
  

