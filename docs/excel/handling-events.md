---
title: Обработка событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807254"
---
# <a name="handling-events"></a><span data-ttu-id="98055-103">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="98055-103">Handling Events</span></span>

 <span data-ttu-id="98055-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98055-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98055-105">Начиная с версии Excel 2010, XLL-модулей может получать события, предназначенное для управления жизненным циклом асинхронные функции.</span><span class="sxs-lookup"><span data-stu-id="98055-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="98055-106">События, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="98055-106">The events are as follows:</span></span>
  
- <span data-ttu-id="98055-107">**CalculationEnded**: возникает, когда завершения вычисления.</span><span class="sxs-lookup"><span data-stu-id="98055-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="98055-108">После этого события можно освободить ресурсы, выделенные в процессе вычисления.</span><span class="sxs-lookup"><span data-stu-id="98055-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="98055-109">**CalculationCanceled**: возникает, когда пользователь прерывает вычисления.</span><span class="sxs-lookup"><span data-stu-id="98055-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="98055-110">XLL останавливает любые асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="98055-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="98055-111">Сразу после этого события **CalculationEnded** событие.</span><span class="sxs-lookup"><span data-stu-id="98055-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="98055-112">Обрабатывать следующие события, XLL использует функции интерфейса API для C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="98055-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="98055-113">**CalculationEnded** и **CalculationCanceled** не возникает во время программный пересчета.</span><span class="sxs-lookup"><span data-stu-id="98055-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

