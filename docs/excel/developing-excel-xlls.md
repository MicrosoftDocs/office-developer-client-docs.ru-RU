---
title: Разработка XLL-модулей для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- надстройки - [excel 2007], разработка XLL-модулей - [Excel 2007], XLL-модулей - [Excel 2007], разработка
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807157"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="80ba2-104">Разработка XLL-модулей для Excel</span><span class="sxs-lookup"><span data-stu-id="80ba2-104">Developing Excel XLLs</span></span>

<span data-ttu-id="80ba2-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="80ba2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="80ba2-106">Главной причиной для записи Microsoft Excel XLL-модулей и с помощью интерфейса API для C — Создание высокопроизводительных функций.</span><span class="sxs-lookup"><span data-stu-id="80ba2-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="80ba2-107">Приложения высокопроизводительные функции — и, начиная с версии Excel 2007, возможность записи многопоточных интерфейсы мощные серверные ресурсы — сделать его важной частью возможностями расширения Excel.</span><span class="sxs-lookup"><span data-stu-id="80ba2-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="80ba2-108">Производительность XLL-модулей для дальнейшей был улучшенные в Excel 2007 путем добавления новых типов данных и, наиболее важные, поддержку многопоточность.</span><span class="sxs-lookup"><span data-stu-id="80ba2-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="80ba2-109">Интерфейса API для C нет более высокого уровня функций быстрой разработки Microsoft Visual Basic для приложений (VBA), COM или Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="80ba2-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="80ba2-110">Управление памятью — низкий уровень и поэтому размещает больше, ответственность за на разработчика.</span><span class="sxs-lookup"><span data-stu-id="80ba2-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="80ba2-111">Многие функции Excel, предоставляемые посредством COM, делая их доступными через VBA и .NET Framework, не представленных C API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80ba2-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="80ba2-112">�������� ���������������� � Excel</span><span class="sxs-lookup"><span data-stu-id="80ba2-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="80ba2-113">Работа с библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="80ba2-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="80ba2-114">Доступ к XLL-коду в Excel</span><span class="sxs-lookup"><span data-stu-id="80ba2-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="80ba2-115">Вызов функции XLL из Мастер функций или заменить диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="80ba2-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="80ba2-116">����� � Excel �� DLL ��� XLL</span><span class="sxs-lookup"><span data-stu-id="80ba2-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="80ba2-117">Создание XLL-модулей</span><span class="sxs-lookup"><span data-stu-id="80ba2-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="80ba2-118">������ ����� � ������ ��������� ������� �����</span><span class="sxs-lookup"><span data-stu-id="80ba2-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="80ba2-119">Многопоточность и управление памятью</span><span class="sxs-lookup"><span data-stu-id="80ba2-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="80ba2-120">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="80ba2-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="80ba2-121">Безопасные для кластера функции</span><span class="sxs-lookup"><span data-stu-id="80ba2-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="80ba2-122">���������� ������������ �������� ������� � ���������� ��������</span><span class="sxs-lookup"><span data-stu-id="80ba2-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="80ba2-123">Отображение диалоговых окон из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="80ba2-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="80ba2-124">Доступ к экземпляру Excel и значками главное окно</span><span class="sxs-lookup"><span data-stu-id="80ba2-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="80ba2-125">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="80ba2-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

