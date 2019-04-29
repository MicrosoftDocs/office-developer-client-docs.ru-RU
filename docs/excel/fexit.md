---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- Функция фексит [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429917"
---
# <a name="fexit"></a><span data-ttu-id="e9e0e-104">fExit</span><span class="sxs-lookup"><span data-stu-id="e9e0e-104">fExit</span></span>

 <span data-ttu-id="e9e0e-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e9e0e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e9e0e-106">Пример пользовательской команды, которая выгружает GENERIC. XLL.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="e9e0e-107">При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="e9e0e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9e0e-108">Parameters</span></span>

<span data-ttu-id="e9e0e-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e9e0e-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9e0e-110">Property value/Return value</span></span>

<span data-ttu-id="e9e0e-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9e0e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9e0e-112">Remarks</span></span>

<span data-ttu-id="e9e0e-113">Эта процедура вызывается пользователем для выхода из УНИВЕРСАЛЬНого объекта. XLL, поэтому не следует `UNREGISTER("GENERIC.XLL")` просто вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="e9e0e-114">При этом будут принудительно отменены все функции в этой библиотеке DLL, даже если они были зарегистрированы в другом месте.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="e9e0e-115">Вместо этого отмените регистрацию функций по одному.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="e9e0e-116">Пример</span><span class="sxs-lookup"><span data-stu-id="e9e0e-116">Example</span></span>

<span data-ttu-id="e9e0e-117">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="e9e0e-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9e0e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e9e0e-118">See also</span></span>



[<span data-ttu-id="e9e0e-119">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="e9e0e-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

