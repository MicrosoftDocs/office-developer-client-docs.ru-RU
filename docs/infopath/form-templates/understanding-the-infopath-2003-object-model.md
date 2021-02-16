---
title: Ознакомление с объектной моделью InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: В этом разделе описана объектная модель для решений InfoPath с управляемым кодом, а также типичные задачи программирования.
ms.openlocfilehash: 0c07201475bb7bfe24182faf61cc1bf6df733709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416659"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="3cba4-104">Общие сведения об объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="3cba4-105">В этом разделе описана объектная модель для решений InfoPath с управляемым кодом, а также типичные задачи программирования.</span><span class="sxs-lookup"><span data-stu-id="3cba4-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3cba4-106">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="3cba4-106">In this section</span></span>

[<span data-ttu-id="3cba4-107">Объектные модели, совместимые с InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="3cba4-108">Предоставляется обзор объектных моделей, используемых в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="3cba4-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="3cba4-109">Доступ к данным приложения с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-110">Описывается доступ к сведениям о приложении InfoPath, базовом XML-документе формы и файле определения формы (XSF).</span><span class="sxs-lookup"><span data-stu-id="3cba4-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="3cba4-111">Доступ к внешним источникам данных с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-112">Описывается доступ к данным, расположенным на внешних источниках данных.</span><span class="sxs-lookup"><span data-stu-id="3cba4-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="3cba4-113">Доступ к данным формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-114">Описывается доступ к сведениям о базовом документе XML для формы и о содержащихся в форме данных, а также выполнение некоторых действий с документом XML.</span><span class="sxs-lookup"><span data-stu-id="3cba4-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="3cba4-115">Отображение оповещений и диалогов с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-116">Описывается отображение оповещений и диалоговых окон в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="3cba4-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="3cba4-117">Обработка ошибок с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-118">Описывается обработка ошибок в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="3cba4-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="3cba4-119">Реагирование на события формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-120">Описывается создание обработчиков событий для обработки событий, возникающих при заполнении пользователем формы.</span><span class="sxs-lookup"><span data-stu-id="3cba4-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="3cba4-121">Работа с Окнами форм с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-122">Описывается работа с окнами форм.</span><span class="sxs-lookup"><span data-stu-id="3cba4-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="3cba4-123">Работа с представлениями с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-124">Описывается работа с представлениями.</span><span class="sxs-lookup"><span data-stu-id="3cba4-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="3cba4-125">Работа с цифровыми подписями с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-126">Описывается работа с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="3cba4-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="3cba4-127">Работа с автономными решениями с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="3cba4-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="3cba4-128">Описывается работа с автономными решениями.</span><span class="sxs-lookup"><span data-stu-id="3cba4-128">Discusses how to work with offline solutions.</span></span>
    

