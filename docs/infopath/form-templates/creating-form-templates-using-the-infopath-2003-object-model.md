---
title: Создание шаблонов форм, использующих объектную модель InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, creating,object models [InfoPath 2003], creating managed code form templates for InfoPath 2007,form templates [InfoPath 2007], creating InfoPath 2003-compatible
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: В этом разделе описана инициализация и очистка кода, добавление обработчиков событий, отладка и развертывание шаблонов форм с управляемым кодом, поддержка потоков и работа со службами MSXML из решений InfoPath с управляемым кодом.
ms.openlocfilehash: 16d49b24b2eed3b7fe15621d47663a94f1958cfa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807478"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="edddb-104">Создание шаблонов форм, использующих объектную модель InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="edddb-105">В этом разделе описана инициализация и очистка кода, добавление обработчиков событий, отладка и развертывание шаблонов форм с управляемым кодом, поддержка потоков и работа со службами MSXML из решений InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="edddb-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="edddb-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="edddb-106">In this section</span></span>

[<span data-ttu-id="edddb-107">Инициализация и очистка кода с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="edddb-108">Описываются методы написания кода инициализации и очистки в методах _Startup и _Shutdown для проекта.</span><span class="sxs-lookup"><span data-stu-id="edddb-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="edddb-109">Добавление обработчика событий с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="edddb-110">Описываются методы добавления обработчиков событий и атрибуты, применяемые идентификации обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="edddb-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="edddb-111">Отладка проектов InfoPath с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="edddb-112">Описываются методы отладки проектов InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="edddb-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="edddb-113">Развертывание шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="edddb-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="edddb-114">Описываются методы развертывания проектов InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="edddb-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="edddb-115">Поддержка потоков в проектах InfoPath, использующих объектную модель InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="edddb-116">Описывается поддержка потоков в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="edddb-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="edddb-117">Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="edddb-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="edddb-118">Описывается работа со службами MSXML и кодом System.Xml в проектах InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="edddb-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

