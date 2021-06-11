---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- функция fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409050"
---
# <a name="fdance"></a><span data-ttu-id="2dc50-104">fDance</span><span class="sxs-lookup"><span data-stu-id="2dc50-104">fDance</span></span>

 <span data-ttu-id="2dc50-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2dc50-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2dc50-106">Пример команды, определяемой пользователем, которая изменяет выбранные ячейки на активном таблице, пока пользователь не нажмет **ESC.**</span><span class="sxs-lookup"><span data-stu-id="2dc50-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="2dc50-107">При загрузке GENERIC.xll создается меню, определяемое пользователем, Generic, с помощью которого получается доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="2dc50-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="2dc50-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="2dc50-108">Parameters</span></span>

<span data-ttu-id="2dc50-109">Функция не принимает параметров.</span><span class="sxs-lookup"><span data-stu-id="2dc50-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2dc50-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dc50-110">Property value/Return value</span></span>

<span data-ttu-id="2dc50-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="2dc50-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dc50-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="2dc50-112">Remarks</span></span>

<span data-ttu-id="2dc50-113">Это пример длительной операции.</span><span class="sxs-lookup"><span data-stu-id="2dc50-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="2dc50-114">Иногда она вызывает [функцию xlAbort.](xlabort.md)</span><span class="sxs-lookup"><span data-stu-id="2dc50-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="2dc50-115">Это дает процессору (помогает совместной многозадачности) и проверяет, нажал ли пользователь **ESC** на отмену операции.</span><span class="sxs-lookup"><span data-stu-id="2dc50-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="2dc50-116">Если это так, он предоставляет пользователю возможность отменить отмену.</span><span class="sxs-lookup"><span data-stu-id="2dc50-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="2dc50-117">Пример</span><span class="sxs-lookup"><span data-stu-id="2dc50-117">Example</span></span>

<span data-ttu-id="2dc50-118">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции.</span><span class="sxs-lookup"><span data-stu-id="2dc50-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2dc50-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2dc50-119">See also</span></span>



[<span data-ttu-id="2dc50-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="2dc50-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

