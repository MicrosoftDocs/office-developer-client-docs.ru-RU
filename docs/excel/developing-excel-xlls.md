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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701097"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="7a82a-104">Разработка XLL-файлов Excel</span><span class="sxs-lookup"><span data-stu-id="7a82a-104">Developing Excel XLLs</span></span>

<span data-ttu-id="7a82a-105">**Область применения**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7a82a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7a82a-106">Основная цель написания XLL-файлов Microsoft Excel и использования API C — создание высокопроизводительных функций.</span><span class="sxs-lookup"><span data-stu-id="7a82a-106">The primary reason for writing XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="7a82a-107">Применения высокопроизводительных функций — и, начиная с Excel 2007, возможность писать многопоточные интерфейсы для мощных серверных ресурсов — делают их очень важной частью расширения Excel.</span><span class="sxs-lookup"><span data-stu-id="7a82a-107">Nevertheless, the applications of high-performance functions—and, in Excel 2013, the ability to write multithreaded interfaces to powerful server resources—make this a very important part of Excel extensibility.</span></span> <span data-ttu-id="7a82a-108">Производительность XLL-файлов была повышена в Excel 2007 путем добавления новых типов данных и, что самое важное, поддержки многопоточности.</span><span class="sxs-lookup"><span data-stu-id="7a82a-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="7a82a-109">В API C нет высокоуровневых функций быстрой разработки на Microsoft Visual Basic для приложений (VBA), COM или Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7a82a-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="7a82a-110">Управление памятью осуществляется на низком уровне, и поэтому возлагает большую ответственность на разработчика.</span><span class="sxs-lookup"><span data-stu-id="7a82a-110">Memory management is low level and, therefore, puts greater responsibility on the developer.</span></span> <span data-ttu-id="7a82a-111">Многие функции Excel, предоставляемые через COM (что делает их доступными через VBA и .NET Framework), недоступны интерфейсу API C.</span><span class="sxs-lookup"><span data-stu-id="7a82a-111">Many Excel features that are exposed via COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="7a82a-112">Понятия, связанные с программированием для Excel</span><span class="sxs-lookup"><span data-stu-id="7a82a-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="7a82a-113">Работа с библиотеками DLL</span><span class="sxs-lookup"><span data-stu-id="7a82a-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="7a82a-114">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="7a82a-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="7a82a-115">Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"</span><span class="sxs-lookup"><span data-stu-id="7a82a-115">Call XLL functions from the Function Wizard or Replace dialog boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="7a82a-116">Вызов Excel из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="7a82a-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="7a82a-117">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="7a82a-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="7a82a-118">Оценка имен и других выражений в формулах листов</span><span class="sxs-lookup"><span data-stu-id="7a82a-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="7a82a-119">Многопоточность и управление памятью</span><span class="sxs-lookup"><span data-stu-id="7a82a-119">Multithreading and memory management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="7a82a-120">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="7a82a-120">Asynchronous user-defined functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="7a82a-121">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="7a82a-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="7a82a-122">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="7a82a-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="7a82a-123">Отображение диалоговых окон из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="7a82a-123">Displaying dialog boxes from within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="7a82a-124">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="7a82a-124">Access Excel instance and main window handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="7a82a-125">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="7a82a-125">Backward compatibility</span></span>](backward-compatibility.md)
  

