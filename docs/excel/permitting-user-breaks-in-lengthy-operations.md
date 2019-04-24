---
title: Разрешение преРывать работу пользователей в длительные операции
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функция xlAbort [Excel 2007], одновременные задачи [Excel 2007], пользовательские перерывы [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310383"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="a0670-104">Разрешение преРывать работу пользователей в длительные операции</span><span class="sxs-lookup"><span data-stu-id="a0670-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="a0670-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a0670-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a0670-106">Несмотря на то, что Windows использует многозадачное прерывание, где выполнение функций или команд может занять длительное время, рекомендуется немедленно получить некоторое время на операционную систему и еще раз, чтобы оно могло запланировать параллельные задачи.</span><span class="sxs-lookup"><span data-stu-id="a0670-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="a0670-107">С помощью собственных вызовов Windows вы можете сделать это с помощью функции Sleep.</span><span class="sxs-lookup"><span data-stu-id="a0670-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="a0670-108">С помощью API C можно сделать это с помощью [функции xlAbort](xlabort.md), которая не только получает обработчик для мгновенного, но также проверяет, нажал ли пользователь клавишу Cancel, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="a0670-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="a0670-109">Таким образом, функция **xlAbort** позволяет коду проверять, желает ли пользователь закончить процесс, выполнить необходимую очистку и вернуть управление в Excel.</span><span class="sxs-lookup"><span data-stu-id="a0670-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="a0670-110">Функция также позволяет очистить условие приостанова.</span><span class="sxs-lookup"><span data-stu-id="a0670-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="a0670-111">Это позволяет командам отображать диалоговое окно, чтобы проверить, хочет ли пользователь завершить команду.</span><span class="sxs-lookup"><span data-stu-id="a0670-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="a0670-112">Если пользователю не требуется завершать команду, вызов функции **xlAbort** с аргументом *false* очищает разрыв.</span><span class="sxs-lookup"><span data-stu-id="a0670-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="a0670-113">(Аргумент Default имеет *значение true* , которое просто проверяет условие, но не очищает его.)</span><span class="sxs-lookup"><span data-stu-id="a0670-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="a0670-114">Вы можете вызвать функцию **xlAbort** из пользовательской функции (UDF) или команды XLL.</span><span class="sxs-lookup"><span data-stu-id="a0670-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="a0670-115">Если функция XlAbort возвращает значение true, то в случае, если функция \*\*\*\* возвращает **значение true**, при обнаружении разрыва пользователя, как правило, будет сокращена функция вычисления функции и возвращено значение, указывающее, что вычисление не было завершено, а может быть ошибкой или нулем.</span><span class="sxs-lookup"><span data-stu-id="a0670-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="a0670-116">Вы не можете очистить условие останова, чтобы другие экземпляры длительных функций, которые также проверяют это условие, также применялись.</span><span class="sxs-lookup"><span data-stu-id="a0670-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="a0670-117">Excel неявно удаляет это условие при завершении пересчета.</span><span class="sxs-lookup"><span data-stu-id="a0670-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="a0670-118">При обнаружении условия останова в команде обычно выполняется очистка условия путем повторного вызова функции **xlAbort** с аргументом **false**, хотя Excel неявно удаляет это условие при завершении команды.</span><span class="sxs-lookup"><span data-stu-id="a0670-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0670-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a0670-119">See also</span></span>



[<span data-ttu-id="a0670-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="a0670-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="a0670-121">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="a0670-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="a0670-122">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="a0670-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="a0670-123">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="a0670-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

