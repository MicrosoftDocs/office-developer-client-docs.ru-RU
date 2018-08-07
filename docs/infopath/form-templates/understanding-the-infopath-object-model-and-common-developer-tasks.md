---
title: Ознакомление с объектной моделью InfoPath и распространенными задачами разработчиков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- examples [infopath 2007],InfoPath 2007, developer tasks,developer tasks [InfoPath 2007],InfoPath 2007, object models,object models [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: В этом разделе предоставляются сведения о типичных задачах разработчиков, возникающих при разработке шаблонов форм InfoPath с управляемым кодом.
ms.openlocfilehash: 9f0bbf36b2533b12ca3f31100c3abc21173d7c6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807594"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="5fcdd-104">Ознакомление с объектной моделью InfoPath и распространенными задачами разработчиков</span><span class="sxs-lookup"><span data-stu-id="5fcdd-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="5fcdd-105">В этом разделе предоставляются сведения о типичных задачах разработчиков, возникающих при разработке шаблонов форм InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5fcdd-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5fcdd-106">In this section</span></span>

[<span data-ttu-id="5fcdd-107">Доступ к данным приложения</span><span class="sxs-lookup"><span data-stu-id="5fcdd-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="5fcdd-108">Описывается доступ к сведениям о приложении InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="5fcdd-109">Обработка событий форм</span><span class="sxs-lookup"><span data-stu-id="5fcdd-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="5fcdd-110">Описывается создание обработчиков событий для обработки событий, возникающих при заполнении пользователем формы.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="5fcdd-111">Доступ к данным форм</span><span class="sxs-lookup"><span data-stu-id="5fcdd-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="5fcdd-112">Описывается доступ к сведениям о базовом документе XML для формы и о содержащихся в форме данных, а также выполнение некоторых действий с документом XML.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="5fcdd-113">Доступ ко внешним источникам данных</span><span class="sxs-lookup"><span data-stu-id="5fcdd-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="5fcdd-114">Описывается доступ к данным, расположенным на внешних источниках данных.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="5fcdd-115">Написание условной логики, определяющей среду выполнения</span><span class="sxs-lookup"><span data-stu-id="5fcdd-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="5fcdd-116">Описывается написание кода, выполняющего различные действия в зависимости от того, где открыта форма: в InfoPath, в веб-браузере или в браузере мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="5fcdd-117">Работа с окнами форм</span><span class="sxs-lookup"><span data-stu-id="5fcdd-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="5fcdd-118">Описывается работа с окнами форм.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="5fcdd-119">Работа с представлениями</span><span class="sxs-lookup"><span data-stu-id="5fcdd-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="5fcdd-120">Описывается работа с представлениями.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="5fcdd-121">Работа с автономными решениями</span><span class="sxs-lookup"><span data-stu-id="5fcdd-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="5fcdd-122">Описывается работа с автономными решениями.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="5fcdd-123">Работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="5fcdd-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="5fcdd-124">Описывается работа с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="5fcdd-125">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="5fcdd-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="5fcdd-126">Описывается обработка ошибок в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="5fcdd-127">Работа с параметрами управления правами на доступ к данным</span><span class="sxs-lookup"><span data-stu-id="5fcdd-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="5fcdd-128">Описывается работа с параметрами управления правами на доступ к данным (IRM).</span><span class="sxs-lookup"><span data-stu-id="5fcdd-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="5fcdd-129">Добавление настраиваемых сборок и ссылок на них</span><span class="sxs-lookup"><span data-stu-id="5fcdd-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="5fcdd-130">Рассматривается добавление в проект шаблона формы пользовательских сборок и ссылок на них.</span><span class="sxs-lookup"><span data-stu-id="5fcdd-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

