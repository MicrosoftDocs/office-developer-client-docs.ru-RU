---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- функция fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807247"
---
# <a name="fexit"></a><span data-ttu-id="b28a3-104">fExit</span><span class="sxs-lookup"><span data-stu-id="b28a3-104">fExit</span></span>

 <span data-ttu-id="b28a3-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b28a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b28a3-106">Пример пользовательской команды, выгружает GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="b28a3-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="b28a3-107">При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.</span><span class="sxs-lookup"><span data-stu-id="b28a3-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="b28a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b28a3-108">Parameters</span></span>

<span data-ttu-id="b28a3-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="b28a3-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b28a3-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b28a3-110">Property value/Return value</span></span>

<span data-ttu-id="b28a3-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="b28a3-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b28a3-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b28a3-112">Remarks</span></span>

<span data-ttu-id="b28a3-113">Это инициированных пользователем процедуру, чтобы выйти из GENERIC.xll следует избегать просто вызова `UNREGISTER("GENERIC.XLL")` в этой функции.</span><span class="sxs-lookup"><span data-stu-id="b28a3-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="b28a3-114">Это будет принудительно отменить регистрацию всех функций в данной библиотеки DLL, даже в том случае, если они являются зарегистрированными где-либо другим способом.</span><span class="sxs-lookup"><span data-stu-id="b28a3-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="b28a3-115">Вместо этого отменить регистрацию функции одному за раз.</span><span class="sxs-lookup"><span data-stu-id="b28a3-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="b28a3-116">Пример</span><span class="sxs-lookup"><span data-stu-id="b28a3-116">Example</span></span>

<span data-ttu-id="b28a3-117">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="b28a3-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b28a3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b28a3-118">See also</span></span>



[<span data-ttu-id="b28a3-119">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="b28a3-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

