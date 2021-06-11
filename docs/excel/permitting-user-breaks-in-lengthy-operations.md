---
title: Разрешение перерывов пользователя в длительных операциях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007], concurrent tasks [Excel 2007], user breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414692"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="7c423-104">Разрешение перерывов пользователя в длительных операциях</span><span class="sxs-lookup"><span data-stu-id="7c423-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="7c423-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c423-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c423-106">Хотя Windows использует устроительный многозадачность, когда выполнение функций или команд может занять много времени, не стоит уступать некоторое время операционной системе, чтобы помочь ей планировать одновременно выполняемые задачи.</span><span class="sxs-lookup"><span data-stu-id="7c423-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="7c423-107">С помощью Windows вызовов можно сделать это с помощью функции сна.</span><span class="sxs-lookup"><span data-stu-id="7c423-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="7c423-108">С помощью API C вы можете сделать это с помощью функции [xlAbort,](xlabort.md)которая не только дает процессор на мгновение, но и проверяет, нажал ли пользователь клавишу отмены, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="7c423-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="7c423-109">Поэтому **функция xlAbort** позволяет коду проверить, хочет ли пользователь закончить процесс, сделать необходимую очистку, а затем вернуть управление Excel.</span><span class="sxs-lookup"><span data-stu-id="7c423-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="7c423-110">Функция также позволяет очистить условие перерыва.</span><span class="sxs-lookup"><span data-stu-id="7c423-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="7c423-111">Это позволяет командам отображать диалоговое окно, чтобы проверить, хочет ли пользователь закончить команду.</span><span class="sxs-lookup"><span data-stu-id="7c423-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="7c423-112">Если пользователь не хочет закончить команду, вызов **функции xlAbort** с аргументом  *FALSE*  снимет разрыв.</span><span class="sxs-lookup"><span data-stu-id="7c423-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="7c423-113">(Аргумент по умолчанию  *true*  , который просто проверяет условие, но не очищает его.)</span><span class="sxs-lookup"><span data-stu-id="7c423-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="7c423-114">Функцию **xlAbort** можно вызвать из пользовательской функции (UDF) или из команды XLL.</span><span class="sxs-lookup"><span data-stu-id="7c423-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="7c423-115">В UDF, когда функция **xlAbort** возвращает **TRUE,** обнаружив перерыв пользователя, обычно вы пресекать вычисление функции и возвращать некоторое значение, чтобы указать, что вычисление не завершено, возможно, ошибка или ноль.</span><span class="sxs-lookup"><span data-stu-id="7c423-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="7c423-116">Условие перерыва не будет очищаться, чтобы другие экземпляры длительных функций, которые также проверяли это условие, также нарушались.</span><span class="sxs-lookup"><span data-stu-id="7c423-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="7c423-117">Excel неявно очищает это условие после окончания пересчета.</span><span class="sxs-lookup"><span data-stu-id="7c423-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="7c423-118">При обнаружении условия перерыва в команде обычно очищается условие путем вызова **функции xlAbort** снова с аргументом **FALSE,** хотя Excel неявно очищает это условие, когда команда заканчивается.</span><span class="sxs-lookup"><span data-stu-id="7c423-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c423-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7c423-119">See also</span></span>



[<span data-ttu-id="7c423-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="7c423-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="7c423-121">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="7c423-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="7c423-122">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="7c423-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="7c423-123">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="7c423-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

