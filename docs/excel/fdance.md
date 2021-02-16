---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- функция fdance [excel 2007]
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
# <a name="fdance"></a><span data-ttu-id="8e281-104">fDance</span><span class="sxs-lookup"><span data-stu-id="8e281-104">fDance</span></span>

 <span data-ttu-id="8e281-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e281-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8e281-106">Пример пользовательской команды, которая изменяет выбранные ячейки активного таблицы, пока пользователь не нажмет **КЛАВИШУ ESC.**</span><span class="sxs-lookup"><span data-stu-id="8e281-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="8e281-107">При загрузке GENERIC.xll создается пользовательское меню Generic, через которое можно получить доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="8e281-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="8e281-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e281-108">Parameters</span></span>

<span data-ttu-id="8e281-109">Функция не принимает никаких параметров.</span><span class="sxs-lookup"><span data-stu-id="8e281-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8e281-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e281-110">Property value/Return value</span></span>

<span data-ttu-id="8e281-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="8e281-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e281-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e281-112">Remarks</span></span>

<span data-ttu-id="8e281-113">Это пример продолжительной операции.</span><span class="sxs-lookup"><span data-stu-id="8e281-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="8e281-114">Она периодически вызывает [функцию xlAbort.](xlabort.md)</span><span class="sxs-lookup"><span data-stu-id="8e281-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="8e281-115">Это дает процессор (помогает совместной многозадачности) и проверяет, нажал ли пользователь **ESC,** чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="8e281-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="8e281-116">В этом случае пользователь может отменить отмену.</span><span class="sxs-lookup"><span data-stu-id="8e281-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="8e281-117">Пример</span><span class="sxs-lookup"><span data-stu-id="8e281-117">Example</span></span>

<span data-ttu-id="8e281-118">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="8e281-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e281-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8e281-119">See also</span></span>



[<span data-ttu-id="8e281-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="8e281-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

