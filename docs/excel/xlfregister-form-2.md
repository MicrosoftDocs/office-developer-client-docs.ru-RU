---
title: xlfRegister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310124"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="edb40-104">xlfRegister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="edb40-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="edb40-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="edb40-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="edb40-106">Может вызываться из команды DLL или XLL, которая вызывается Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="edb40-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="edb40-107">Это эквивалентно вызову **Register** из листа макросов Microsoft Office XLM.</span><span class="sxs-lookup"><span data-stu-id="edb40-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="edb40-108">Функцию **xlfRegister** можно вызвать в двух формах:</span><span class="sxs-lookup"><span data-stu-id="edb40-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="edb40-109">[xlfRegister (форма 1)](xlfregister-form-1.md): регистрирует отдельные команды или функции.</span><span class="sxs-lookup"><span data-stu-id="edb40-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="edb40-110">xlfRegister (форма 2): Загрузка и активация XLL-модуля.</span><span class="sxs-lookup"><span data-stu-id="edb40-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="edb40-111">Эта функция, выЗываемая в форме 2, может использоваться только для загрузки и активации XLL, содержащего процедуру [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="edb40-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="edb40-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="edb40-112">Parameters</span></span>

 <span data-ttu-id="edb40-113">_пксмодулетекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="edb40-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="edb40-114">Имя библиотеки DLL, которая должна быть загружена и активирована.</span><span class="sxs-lookup"><span data-stu-id="edb40-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="edb40-115">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edb40-115">Property value/Return value</span></span>

<span data-ttu-id="edb40-116">В случае успешного выполнения возвращается имя DLL (**кслтипестр**).</span><span class="sxs-lookup"><span data-stu-id="edb40-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="edb40-117">В противном случае возвращается #VALUE!</span><span class="sxs-lookup"><span data-stu-id="edb40-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="edb40-118">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="edb40-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb40-119">См. также</span><span class="sxs-lookup"><span data-stu-id="edb40-119">See also</span></span>



[<span data-ttu-id="edb40-120">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="edb40-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

