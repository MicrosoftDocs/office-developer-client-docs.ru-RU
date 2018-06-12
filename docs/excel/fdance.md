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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807260"
---
# <a name="fdance"></a><span data-ttu-id="ee578-104">fDance</span><span class="sxs-lookup"><span data-stu-id="ee578-104">fDance</span></span>

 <span data-ttu-id="ee578-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ee578-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ee578-106">Пример пользовательской команды, изменения выбранных ячеек на активном листе вокруг только при нажатии клавиши **ESC**.</span><span class="sxs-lookup"><span data-stu-id="ee578-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="ee578-107">При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.</span><span class="sxs-lookup"><span data-stu-id="ee578-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="ee578-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee578-108">Parameters</span></span>

<span data-ttu-id="ee578-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="ee578-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ee578-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee578-110">Property value/Return value</span></span>

<span data-ttu-id="ee578-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="ee578-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee578-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee578-112">Remarks</span></span>

<span data-ttu-id="ee578-113">Это пример длительной операции.</span><span class="sxs-lookup"><span data-stu-id="ee578-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="ee578-114">Периодически вызывает функцию [xlAbort](xlabort.md) .</span><span class="sxs-lookup"><span data-stu-id="ee578-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="ee578-115">Это дает процессора (помощь с совместной работой многозадачность) и проверяет нажатии пользователем клавиши **ESC** , чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="ee578-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="ee578-116">Если это так, предлагает пользователю возможность отменить аварийное завершение.</span><span class="sxs-lookup"><span data-stu-id="ee578-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="ee578-117">Пример</span><span class="sxs-lookup"><span data-stu-id="ee578-117">Example</span></span>

<span data-ttu-id="ee578-118">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="ee578-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee578-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ee578-119">See also</span></span>



[<span data-ttu-id="ee578-120">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="ee578-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

