---
title: Обработка событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438269"
---
# <a name="handling-events"></a><span data-ttu-id="cb949-103">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="cb949-103">Handling Events</span></span>

 <span data-ttu-id="cb949-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb949-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb949-105">Начиная с Excel 2010 XLL могут получать события, предназначенные для управления жизненным циклом асинхронной функции.</span><span class="sxs-lookup"><span data-stu-id="cb949-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="cb949-106">Ниже приведены события.</span><span class="sxs-lookup"><span data-stu-id="cb949-106">The events are as follows:</span></span>
  
- <span data-ttu-id="cb949-107">**Калкулатионендед**: вызывается после завершения вычисления Excel.</span><span class="sxs-lookup"><span data-stu-id="cb949-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="cb949-108">После этого события можно освободить ресурсы, выделенные во время вычисления.</span><span class="sxs-lookup"><span data-stu-id="cb949-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="cb949-109">**Калкулатионканцелед**: вызывается, когда пользователь прерывает вычисление.</span><span class="sxs-lookup"><span data-stu-id="cb949-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="cb949-110">XLL остановить все асинхронные действия.</span><span class="sxs-lookup"><span data-stu-id="cb949-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="cb949-111">Сразу после этого события вызывается событие **калкулатионендед** .</span><span class="sxs-lookup"><span data-stu-id="cb949-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="cb949-112">Для обработки этих событий XLL использует функцию C API [кслевентрегистер](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb949-113">**Калкулатионендед** и **калкулатионканцелед** не вызываются во время программного пересчета.</span><span class="sxs-lookup"><span data-stu-id="cb949-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

