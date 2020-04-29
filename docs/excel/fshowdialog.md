---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- Функция фшовдиалог [Excel 2007]
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
# <a name="fshowdialog"></a><span data-ttu-id="de02a-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="de02a-104">fShowDialog</span></span>

 <span data-ttu-id="de02a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de02a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="de02a-106">Пример пользовательской команды, которая загружает и отображает пример собственного диалогового окна Windows.</span><span class="sxs-lookup"><span data-stu-id="de02a-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="de02a-107">При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="de02a-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="de02a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de02a-108">Parameters</span></span>

<span data-ttu-id="de02a-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="de02a-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="de02a-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de02a-110">Property value/Return value</span></span>

<span data-ttu-id="de02a-111">Функция возвращает целочисленный ноль, указывающий на успешность выполнения</span><span class="sxs-lookup"><span data-stu-id="de02a-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de02a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="de02a-112">Remarks</span></span>

<span data-ttu-id="de02a-113">Ниже приведены действия по отображению собственного диалогового окна Windows.</span><span class="sxs-lookup"><span data-stu-id="de02a-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="de02a-114">Получите основной дескриптор Windows **Excel с помощью**метода getHandler.</span><span class="sxs-lookup"><span data-stu-id="de02a-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="de02a-115">Подключите главное окно Excel с помощью **хукексцелвиндов**.</span><span class="sxs-lookup"><span data-stu-id="de02a-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="de02a-116">Откройте диалоговое окно с помощью **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="de02a-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="de02a-117">Отсоедините главное окно Excel с помощью **унхукексцелвиндов**.</span><span class="sxs-lookup"><span data-stu-id="de02a-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="de02a-118">Пример</span><span class="sxs-lookup"><span data-stu-id="de02a-118">Example</span></span>

<span data-ttu-id="de02a-119">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="de02a-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de02a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="de02a-120">See also</span></span>



[<span data-ttu-id="de02a-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="de02a-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

