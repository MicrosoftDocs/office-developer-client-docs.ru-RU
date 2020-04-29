---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- Функция фданце [Excel 2007]
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
# <a name="fdance"></a><span data-ttu-id="580a4-104">fDance</span><span class="sxs-lookup"><span data-stu-id="580a4-104">fDance</span></span>

 <span data-ttu-id="580a4-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="580a4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="580a4-106">Пример пользовательской команды, которая изменяет выбранные ячейки на активном листе до тех пор, пока пользователь не нажмет клавишу **ESC**.</span><span class="sxs-lookup"><span data-stu-id="580a4-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="580a4-107">При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="580a4-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="580a4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="580a4-108">Parameters</span></span>

<span data-ttu-id="580a4-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="580a4-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="580a4-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="580a4-110">Property value/Return value</span></span>

<span data-ttu-id="580a4-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="580a4-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="580a4-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="580a4-112">Remarks</span></span>

<span data-ttu-id="580a4-113">Это пример длительной операции.</span><span class="sxs-lookup"><span data-stu-id="580a4-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="580a4-114">Он иногда вызывает функцию [xlAbort](xlabort.md) .</span><span class="sxs-lookup"><span data-stu-id="580a4-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="580a4-115">Это дает процессор (способствует совместной работе с многозадачными задачами) и проверяет, нажал ли пользователь клавишу **ESC** , чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="580a4-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="580a4-116">Если да, то пользователь может отменить прерывание.</span><span class="sxs-lookup"><span data-stu-id="580a4-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="580a4-117">Пример</span><span class="sxs-lookup"><span data-stu-id="580a4-117">Example</span></span>

<span data-ttu-id="580a4-118">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="580a4-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="580a4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="580a4-119">See also</span></span>



[<span data-ttu-id="580a4-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="580a4-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

