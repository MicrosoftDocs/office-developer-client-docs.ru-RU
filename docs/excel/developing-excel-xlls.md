---
title: Разработка XLL-файлов Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- надстройки — [excel 2007], разработка XLL-файлов — [Excel 2007], XLL-файлы — [Excel 2007], разработка
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301661"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="f92a0-104">Разработка XLL-файлов Excel</span><span class="sxs-lookup"><span data-stu-id="f92a0-104">Developing Excel XLLs</span></span>

<span data-ttu-id="f92a0-105">**Область применения**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f92a0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f92a0-106">Основная цель написания XLL-файлов Microsoft Excel и использования API C — создание высокопроизводительных функций.</span><span class="sxs-lookup"><span data-stu-id="f92a0-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="f92a0-107">Применения высокопроизводительных функций — и, начиная с Excel 2007, возможность писать многопоточные интерфейсы для мощных серверных ресурсов — делают их очень важной частью расширения Excel.</span><span class="sxs-lookup"><span data-stu-id="f92a0-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="f92a0-108">Производительность XLL-файлов была повышена в Excel 2007 путем добавления новых типов данных и, что самое важное, поддержки многопоточности.</span><span class="sxs-lookup"><span data-stu-id="f92a0-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="f92a0-109">В API C нет высокоуровневых функций быстрой разработки на Microsoft Visual Basic для приложений (VBA), COM или Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f92a0-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="f92a0-110">Управление памятью осуществляется на низком уровне, и поэтому возлагает большую ответственность на разработчика.</span><span class="sxs-lookup"><span data-stu-id="f92a0-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="f92a0-111">Многие функции Excel, предоставляемые через COM (что делает их доступными через VBA и .NET Framework), недоступны интерфейсу API C.</span><span class="sxs-lookup"><span data-stu-id="f92a0-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="f92a0-112">Понятия, связанные с программированием для Excel</span><span class="sxs-lookup"><span data-stu-id="f92a0-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="f92a0-113">Работа с библиотеками DLL</span><span class="sxs-lookup"><span data-stu-id="f92a0-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="f92a0-114">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="f92a0-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="f92a0-115">Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"</span><span class="sxs-lookup"><span data-stu-id="f92a0-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="f92a0-116">Вызов Excel из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f92a0-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="f92a0-117">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="f92a0-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="f92a0-118">Оценка имен и других выражений в формулах листов</span><span class="sxs-lookup"><span data-stu-id="f92a0-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="f92a0-119">Многопоточность и управление памятью</span><span class="sxs-lookup"><span data-stu-id="f92a0-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="f92a0-120">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="f92a0-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="f92a0-121">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="f92a0-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="f92a0-122">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="f92a0-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="f92a0-123">Отображение диалоговых окон из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f92a0-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="f92a0-124">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="f92a0-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="f92a0-125">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="f92a0-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

