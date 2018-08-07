---
title: Разрешение прерывания длительных операций пользователем
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функция xlAbort [excel 2007,] параллельных задач [Excel 2007], разрывов пользователя [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807312"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="c9992-104">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="c9992-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="c9992-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c9992-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c9992-106">Несмотря на то, что используется Windows включить многозадачность, где функции или команды может занять много времени на выполнение, рекомендуется, чтобы получить некоторое время для операционной системы и для ее планирования параллельных задач.</span><span class="sxs-lookup"><span data-stu-id="c9992-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="c9992-107">С помощью собственного вызовов Windows, можно сделать это с помощью функции спящего режима.</span><span class="sxs-lookup"><span data-stu-id="c9992-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="c9992-108">Использование интерфейса API для C, можно сделать его с помощью [функции xlAbort](xlabort.md), который не только дает процессора для обмена мгновенными, но также проверяет, если пользователь нажата клавиша cancel, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="c9992-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="c9992-109">Функция **xlAbort** таким образом включает код для проверки, является ли пользователю необходимо завершить процесс, выполните необходимые очистки и затем вернуться элемента управления в Excel.</span><span class="sxs-lookup"><span data-stu-id="c9992-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="c9992-110">Функция также позволяет очистить условия останова.</span><span class="sxs-lookup"><span data-stu-id="c9992-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="c9992-111">Это позволяет команды для отображения диалогового окна Проверка ли пользователь хочет завершения команды.</span><span class="sxs-lookup"><span data-stu-id="c9992-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="c9992-112">Если пользователь не нужно закончить команды, вызов функции **xlAbort** с аргументом *FALSE* очищает приостановки выполнения.</span><span class="sxs-lookup"><span data-stu-id="c9992-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="c9992-113">(Аргумент по умолчанию используется *значение TRUE* , которое просто проверяет условие, но не очищает.)</span><span class="sxs-lookup"><span data-stu-id="c9992-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="c9992-114">Можно вызвать функцию **xlAbort** из пользовательской функции (UDF) или команду XLL.</span><span class="sxs-lookup"><span data-stu-id="c9992-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="c9992-115">В пользовательской функции функция **xlAbort** возвращает **значение TRUE**, обнаружен разрыв пользователя необходимо обычно Вырезать короткий вычисления функции и возврата некоторые значение, указывающее, что расчет завершилось завершено, возможно сообщение об ошибке или ноль.</span><span class="sxs-lookup"><span data-stu-id="c9992-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="c9992-116">Вы не снять условие приостановки выполнения, чтобы другие экземпляры длительным функций, которые также проверить это условие также разрыв.</span><span class="sxs-lookup"><span data-stu-id="c9992-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="c9992-117">Excel неявно очищает это условие, при завершении пересчета.</span><span class="sxs-lookup"><span data-stu-id="c9992-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="c9992-118">Если в команду обнаружить условия останова, обычно снять условие путем вызова функции **xlAbort** еще раз с аргументом, **значение FALSE**, несмотря на то, что Excel неявно очищает это условие при завершении команды.</span><span class="sxs-lookup"><span data-stu-id="c9992-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9992-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c9992-119">See also</span></span>



[<span data-ttu-id="c9992-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="c9992-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="c9992-121">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="c9992-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="c9992-122">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="c9992-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="c9992-123">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="c9992-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

