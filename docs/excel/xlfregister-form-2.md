---
title: xlfRegister (формы 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807350"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="037b2-104">xlfRegister (формы 2)</span><span class="sxs-lookup"><span data-stu-id="037b2-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="037b2-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="037b2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="037b2-106">Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="037b2-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="037b2-107">Это эквивалентно вызову **регистрации** из таблицы Excel XLM макрос.</span><span class="sxs-lookup"><span data-stu-id="037b2-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="037b2-108">Функция **xlfRegister** может быть вызвана в двух вариантах:</span><span class="sxs-lookup"><span data-stu-id="037b2-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="037b2-109">[xlfRegister (формы 1)](xlfregister-form-1.md): регистрирует отдельные команды или функции.</span><span class="sxs-lookup"><span data-stu-id="037b2-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="037b2-110">xlfRegister (формы 2): загружает и активирует надстройке XLL.</span><span class="sxs-lookup"><span data-stu-id="037b2-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="037b2-111">Вызывает в виде 2, эта функция может использоваться только для загружать и активировать XLL, содержащий процедуру [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="037b2-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="037b2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="037b2-112">Parameters</span></span>

 <span data-ttu-id="037b2-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="037b2-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="037b2-114">Имя библиотеки DLL, загружать и активирован.</span><span class="sxs-lookup"><span data-stu-id="037b2-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="037b2-115">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="037b2-115">Property value/Return value</span></span>

<span data-ttu-id="037b2-116">В случае успешного выполнения возвращает имя DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="037b2-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="037b2-117">В противном случае возвращается #VALUE!</span><span class="sxs-lookup"><span data-stu-id="037b2-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="037b2-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="037b2-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="037b2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="037b2-119">See also</span></span>



[<span data-ttu-id="037b2-120">Функции API XLM важные и полезные C</span><span class="sxs-lookup"><span data-stu-id="037b2-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

