---
title: Функции вызова API C Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [excel 2007], вызов API c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434433"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="184c8-104">Функции вызова API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="184c8-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="184c8-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="184c8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="184c8-106">Функции **Excel4** и **Excel12** позволяют DLL вызывать внутреннюю функцию листа Microsoft Excel, функцию или команду листа макроса или специальную функцию или команду только для XLL.</span><span class="sxs-lookup"><span data-stu-id="184c8-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="184c8-107">Все последние версии Excel поддерживают **функцию Excel4.**</span><span class="sxs-lookup"><span data-stu-id="184c8-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="184c8-108">Начиная с Excel 2007 функция **Excel12** поддерживается.</span><span class="sxs-lookup"><span data-stu-id="184c8-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="184c8-109">Обе функции предоставляются в двух формах:</span><span class="sxs-lookup"><span data-stu-id="184c8-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="184c8-110">Форма списка аргументов переменной длины (**Excel4/Excel12)**</span><span class="sxs-lookup"><span data-stu-id="184c8-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="184c8-111">Форма массива аргументов (**Excel4v/Excel12v)**</span><span class="sxs-lookup"><span data-stu-id="184c8-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="184c8-112">За исключением способа, которым аргументы передаются в эти функции, эти две формы являются функционально эквивалентными.</span><span class="sxs-lookup"><span data-stu-id="184c8-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="184c8-113">Основные понятия для обеих форм полностью описаны в [Excel4/Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="184c8-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="184c8-114">[Excel4v/Excel12v](excel4v-excel12v.md) охватывает другие проблемы, которые могут быть у этой формы.</span><span class="sxs-lookup"><span data-stu-id="184c8-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="184c8-115">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="184c8-115">In this section</span></span>

[<span data-ttu-id="184c8-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="184c8-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="184c8-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="184c8-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

