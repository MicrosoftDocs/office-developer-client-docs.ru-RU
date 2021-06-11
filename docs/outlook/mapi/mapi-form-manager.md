---
title: Диспетчер форм MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430198"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="4c13b-103">Диспетчер форм MAPI</span><span class="sxs-lookup"><span data-stu-id="4c13b-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="4c13b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c13b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c13b-105">Диспетчер форм — это объект, реализуя [интерфейс IMAPIFormMgr.](imapiformmgriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4c13b-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="4c13b-106">Большинство организаций будут использовать диспетчер форм, поставляемый с MAPI, именуемой диспетчером форм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c13b-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="4c13b-107">Однако при желании организация может заменить диспетчера форм по умолчанию настраиваемой диспетчером форм.</span><span class="sxs-lookup"><span data-stu-id="4c13b-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="4c13b-108">Руководитель форм заботится о поиске форм в библиотеках форм, загрузке форм в ответ на запросы пользователей и установке форм в локализованную библиотеку форм пользователя, библиотеку форм папок или личную библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="4c13b-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="4c13b-109">Чтобы пользователь взаимодействовал с сообщением, необходимо создать и активировать экземпляр сервера формы для класса сообщений для отображения сообщения и выполнения запрашиваемой операции в сообщении.</span><span class="sxs-lookup"><span data-stu-id="4c13b-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="4c13b-110">Как описано в разделе [MapI Form Libraries,](mapi-form-libraries.md)реализация формы может существовать в нескольких различных расположениях (библиотеках форм), и нет никакой гарантии, что форма или ее сервер будут доступны локально или в запущенном состоянии, когда пользователь хочет взаимодействовать с ней.</span><span class="sxs-lookup"><span data-stu-id="4c13b-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="4c13b-111">Диспетчер форм заботится о деталях размещения и активации формы.</span><span class="sxs-lookup"><span data-stu-id="4c13b-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="4c13b-112">Клиенты используют службы, предоставляемые менеджером форм, для поиска и активации форм.</span><span class="sxs-lookup"><span data-stu-id="4c13b-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="4c13b-113">Интерфейс **IMAPIFormMgr** реализован менеджером форм и вызван клиентами для доступа к его службам.</span><span class="sxs-lookup"><span data-stu-id="4c13b-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="4c13b-114">Менеджер формы является важным компонентом, так как он скрывает почти все сведения о поиске и активации форм от клиентов обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4c13b-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="4c13b-115">При загрузке серверов форм диспетчер форм по умолчанию загружает форму из первой библиотеки форм, в которой находится реализация для класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="4c13b-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="4c13b-116">Менеджер форм по умолчанию ищет библиотеки форм в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="4c13b-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="4c13b-117">Локализованная библиотека форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c13b-117">The user's local form library.</span></span> <span data-ttu-id="4c13b-118">Сначала эта библиотека форм будет искаться, так как обеспечивает самый быстрый доступ к реализации формы, если реализация установлена в локальной библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="4c13b-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="4c13b-119">Библиотека форм папки контейнера сообщения — папка, в которой загружается сообщение.</span><span class="sxs-lookup"><span data-stu-id="4c13b-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="4c13b-120">Библиотека личной формы пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c13b-120">The user's personal form library.</span></span>
    
<span data-ttu-id="4c13b-121">Настраиваемый диспетчер форм может выполнять поиск доступных библиотек форм в любом порядке или реализовать другие библиотеки форм, такие как библиотека форм для всей организации.</span><span class="sxs-lookup"><span data-stu-id="4c13b-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="4c13b-122">Дополнительные сведения о библиотеках форм см. в [материале MAPI Form Libraries.](mapi-form-libraries.md)</span><span class="sxs-lookup"><span data-stu-id="4c13b-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c13b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4c13b-123">See also</span></span>



[<span data-ttu-id="4c13b-124">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="4c13b-124">MAPI Forms</span></span>](mapi-forms.md)

