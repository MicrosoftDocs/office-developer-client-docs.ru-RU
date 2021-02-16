---
title: ДИСПЕТЧЕР форм MAPI
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
# <a name="mapi-form-manager"></a><span data-ttu-id="f7874-103">ДИСПЕТЧЕР форм MAPI</span><span class="sxs-lookup"><span data-stu-id="f7874-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="f7874-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7874-105">Диспетчер форм — это объект, который реализует [интерфейс IMAPIFormMgr.](imapiformmgriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f7874-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="f7874-106">В большинстве организаций используется диспетчер форм, поставляный с MAPI, который называется диспетчером форм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7874-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="f7874-107">Однако при необходимости организация может заменить диспетчер форм по умолчанию на настраиваемый диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="f7874-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="f7874-108">Диспетчер форм осуществляет поиск форм в библиотеках форм, загрузку форм в ответ на запросы пользователей и установку форм в локализованную библиотеку форм пользователя, библиотеку форм папок или личную библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="f7874-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="f7874-109">Чтобы пользователь взаимодействовал с сообщением, необходимо создать и активировать экземпляр сервера форм для класса сообщения, чтобы отобразить сообщение и выполнить запрашиваемую операцию с сообщением.</span><span class="sxs-lookup"><span data-stu-id="f7874-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="f7874-110">Как описано в разделе "Библиотеки форм [MAPI",](mapi-form-libraries.md)реализация формы может существовать в нескольких различных расположениях (библиотеках форм), и нет гарантии, что форма или ее сервер будут доступны локально или в запущенном состоянии, когда пользователь хочет взаимодействовать с ней.</span><span class="sxs-lookup"><span data-stu-id="f7874-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="f7874-111">Диспетчер форм берет на себя сведения о поиске и активации формы.</span><span class="sxs-lookup"><span data-stu-id="f7874-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="f7874-112">Клиенты используют службы, предоставляемые диспетчером форм, для поиска и активации форм.</span><span class="sxs-lookup"><span data-stu-id="f7874-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="f7874-113">Интерфейс **IMAPIFormMgr** реализован диспетчером форм и вызван клиентами для доступа к его службам.</span><span class="sxs-lookup"><span data-stu-id="f7874-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="f7874-114">Диспетчер форм является важным компонентом, так как он скрывает почти все сведения о поиске и активации форм из клиентов обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f7874-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="f7874-115">При загрузке серверов форм диспетчер форм по умолчанию загружает форму из первой библиотеки форм, в которой найдена реализация класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="f7874-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="f7874-116">Диспетчер форм по умолчанию выполняет поиск в библиотеках форм в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="f7874-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="f7874-117">Локализованная библиотека форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7874-117">The user's local form library.</span></span> <span data-ttu-id="f7874-118">В этой библиотеке форм сначала ведется поиск, так как она обеспечивает самый быстрый доступ к реализации формы, если реализация установлена в локальной библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="f7874-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="f7874-119">Библиотека форм папки контейнера сообщения — папка, в которую загружается сообщение.</span><span class="sxs-lookup"><span data-stu-id="f7874-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="f7874-120">Личная библиотека форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7874-120">The user's personal form library.</span></span>
    
<span data-ttu-id="f7874-121">Настраиваемый диспетчер форм может выполнять поиск в доступных библиотеках форм в любом порядке или реализовать другие библиотеки форм, например библиотеку форм для всей организации.</span><span class="sxs-lookup"><span data-stu-id="f7874-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="f7874-122">Дополнительные сведения о библиотеках форм см. в [библиотеке форм MAPI.](mapi-form-libraries.md)</span><span class="sxs-lookup"><span data-stu-id="f7874-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7874-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f7874-123">See also</span></span>



[<span data-ttu-id="f7874-124">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="f7874-124">MAPI Forms</span></span>](mapi-forms.md)

