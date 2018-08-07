---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- функция fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807266"
---
# <a name="fshowdialog"></a><span data-ttu-id="15d12-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="15d12-104">fShowDialog</span></span>

 <span data-ttu-id="15d12-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="15d12-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="15d12-106">Пример пользовательской команды, загружает и отображает пример собственный диалоговое окно Windows.</span><span class="sxs-lookup"><span data-stu-id="15d12-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="15d12-107">При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.</span><span class="sxs-lookup"><span data-stu-id="15d12-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="15d12-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15d12-108">Parameters</span></span>

<span data-ttu-id="15d12-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="15d12-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="15d12-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15d12-110">Property value/Return value</span></span>

<span data-ttu-id="15d12-111">Функция возвращаемое целое число ноль для указания успешное завершение работы</span><span class="sxs-lookup"><span data-stu-id="15d12-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15d12-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="15d12-112">Remarks</span></span>

<span data-ttu-id="15d12-113">Доступны следующие действия, чтобы открыть диалоговое окно собственного Windows:</span><span class="sxs-lookup"><span data-stu-id="15d12-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="15d12-114">Получите Microsoft Excel основной обработчик Windows с помощью **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="15d12-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="15d12-115">Внедрение главного окна Excel с помощью **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="15d12-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="15d12-116">Отображать диалоговое окно с помощью **следующейтаблице**.</span><span class="sxs-lookup"><span data-stu-id="15d12-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="15d12-117">Отсоедините главного окна Excel с помощью **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="15d12-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="15d12-118">Пример</span><span class="sxs-lookup"><span data-stu-id="15d12-118">Example</span></span>

<span data-ttu-id="15d12-119">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="15d12-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15d12-120">См. также</span><span class="sxs-lookup"><span data-stu-id="15d12-120">See also</span></span>



[<span data-ttu-id="15d12-121">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="15d12-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

