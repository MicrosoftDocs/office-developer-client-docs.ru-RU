---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- Функция fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433593"
---
# <a name="fshowdialog"></a><span data-ttu-id="a155f-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="a155f-104">fShowDialog</span></span>

 <span data-ttu-id="a155f-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a155f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a155f-106">Пример пользовательской команды, которая загружает и отображает пример нативного диалоговое окно Windows.</span><span class="sxs-lookup"><span data-stu-id="a155f-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="a155f-107">При загрузке GENERIC.xll создается пользовательское меню Generic, через которое можно получить доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="a155f-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="a155f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a155f-108">Parameters</span></span>

<span data-ttu-id="a155f-109">Функция не принимает никаких параметров.</span><span class="sxs-lookup"><span data-stu-id="a155f-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a155f-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a155f-110">Property value/Return value</span></span>

<span data-ttu-id="a155f-111">Функция возвращает нулевое значение, чтобы указать успешное завершение</span><span class="sxs-lookup"><span data-stu-id="a155f-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a155f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a155f-112">Remarks</span></span>

<span data-ttu-id="a155f-113">Чтобы отобразить диалоговое окно Windows, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a155f-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="a155f-114">Получите основной лад Windows Microsoft Excel с помощью **GetHwnd.**</span><span class="sxs-lookup"><span data-stu-id="a155f-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="a155f-115">Подключите главное окно Excel с помощью **HookExcelWindow.**</span><span class="sxs-lookup"><span data-stu-id="a155f-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="a155f-116">Отобразите диалоговое окно с помощью **DialogBox.**</span><span class="sxs-lookup"><span data-stu-id="a155f-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="a155f-117">Отогнали главное окно Excel с помощью **UnhookExcelWindow.**</span><span class="sxs-lookup"><span data-stu-id="a155f-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="a155f-118">Пример</span><span class="sxs-lookup"><span data-stu-id="a155f-118">Example</span></span>

<span data-ttu-id="a155f-119">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="a155f-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a155f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a155f-120">See also</span></span>



[<span data-ttu-id="a155f-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="a155f-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

