---
title: xlfRegister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfregister [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416043"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="65238-104">xlfRegister (форма 2)</span><span class="sxs-lookup"><span data-stu-id="65238-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="65238-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="65238-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="65238-106">Может быть вызвано из команды DLL или XLL, которая сама была вызвана Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="65238-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="65238-107">Это эквивалентно вызову **REGISTER** с макрос Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="65238-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="65238-108">Функцию **xlfRegister** можно назвать в двух формах:</span><span class="sxs-lookup"><span data-stu-id="65238-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="65238-109">[xlfRegister (Форма 1)](xlfregister-form-1.md): Регистрирует индивидуальную команду или функцию.</span><span class="sxs-lookup"><span data-stu-id="65238-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="65238-110">xlfRegister (Форма 2): Загружает и активирует XLL.</span><span class="sxs-lookup"><span data-stu-id="65238-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="65238-111">Вызванная в форме 2, эта функция может использоваться только для загрузки и активации XLL, содержащей [процедуру xlAutoOpen.](xlautoopen.md)</span><span class="sxs-lookup"><span data-stu-id="65238-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="65238-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="65238-112">Parameters</span></span>

 <span data-ttu-id="65238-113">_pxModuleText_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="65238-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="65238-114">Имя DLL для загрузки и активации.</span><span class="sxs-lookup"><span data-stu-id="65238-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="65238-115">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65238-115">Property value/Return value</span></span>

<span data-ttu-id="65238-116">В случае успешной работы возвращается имя DLL **(xltypeStr).**</span><span class="sxs-lookup"><span data-stu-id="65238-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="65238-117">В противном случае он возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="65238-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="65238-118">ошибка.</span><span class="sxs-lookup"><span data-stu-id="65238-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65238-119">См. также</span><span class="sxs-lookup"><span data-stu-id="65238-119">See also</span></span>



[<span data-ttu-id="65238-120">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="65238-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

