---
title: Реализация просмотра форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435819"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="a8025-103">Реализация просмотра форм</span><span class="sxs-lookup"><span data-stu-id="a8025-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="a8025-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8025-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8025-105">Зритель формы включает в себя три объекта: сайт сообщения, представление рекомендации раковины и контекст представления.</span><span class="sxs-lookup"><span data-stu-id="a8025-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="a8025-106">Каждый из этих объектов позволяет взаимодействовать с сервером форм и его формами.</span><span class="sxs-lookup"><span data-stu-id="a8025-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="a8025-107">Сайт сообщений — это объект, реализующий [интерфейс IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) и помогающий серверам форм с такими задачами, как перемещение, сохранение или удаление сообщений, создание новых сообщений или запуск новых серверов форм.</span><span class="sxs-lookup"><span data-stu-id="a8025-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="a8025-108">Сайты сообщений используются формами для получения сведений о состоянии клиента в отношении различных поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a8025-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="a8025-109">Например, форма может использовать ваш сайт сообщений для получения указателя в текущем хранилище сообщений, сообщении или папке.</span><span class="sxs-lookup"><span data-stu-id="a8025-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="a8025-110">В интерфейсе **IMAPIMessageSite** существует два типа методов:</span><span class="sxs-lookup"><span data-stu-id="a8025-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="a8025-111">Методы, которые предоставляют информацию для формирования объектов.</span><span class="sxs-lookup"><span data-stu-id="a8025-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="a8025-112">Методы, которые манипулируют сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a8025-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="a8025-113">Методы, которые предоставляют информацию для формирования объектов, просты в реализации.</span><span class="sxs-lookup"><span data-stu-id="a8025-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="a8025-114">Во всех случаях, кроме [IMAPIMessageSite::GetSiteStatus,](imapimessagesite-getsitestatus.md)вы уже должны иметь доступ к информации, требуемой каждым методом.</span><span class="sxs-lookup"><span data-stu-id="a8025-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="a8025-115">Методы, которые манипулируют сообщениями, должны действовать так, как если бы они были вызваны с помощью обычного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8025-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="a8025-116">Например, если объект формы вызывает метод [IMAPIMessageSite::NewMessage,](imapimessagesite-newmessage.md) ведите себя так, будто пользователь решил составить новое пользовательское сообщение с помощью обычного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8025-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="a8025-117">Команды, которые обычно генерируют такое поведение: **Compose,** **Open,** **Reply,** **Reply to All Recipients** и **Forward**.</span><span class="sxs-lookup"><span data-stu-id="a8025-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="a8025-118">Контекст представления — это объект, который реализует [интерфейс IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) и предоставляет серверам форм контекст для текущего сообщения, что позволяет серверам легко переключаться на следующее или предыдущее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="a8025-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="a8025-119">Форма использует контекст представления для обмена информацией.</span><span class="sxs-lookup"><span data-stu-id="a8025-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="a8025-120">С объектом контекста представления форма может:</span><span class="sxs-lookup"><span data-stu-id="a8025-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="a8025-121">Зарегистрируйтесь у клиента для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8025-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="a8025-122">Активируйте следующее или предыдущее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="a8025-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="a8025-123">Получить сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="a8025-123">Get printing information.</span></span>
    
- <span data-ttu-id="a8025-124">Получите состояние клиента.</span><span class="sxs-lookup"><span data-stu-id="a8025-124">Get your client's status.</span></span>
    
- <span data-ttu-id="a8025-125">Получите поток, который можно использовать для сохранения текстовой версии сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8025-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="a8025-126">Как и методы в [интерфейсе IMAPIMessageSite: IUnknown,](imapimessagesiteiunknown.md) методы **в IMAPIViewContext** соотносятся с действиями пользователей и функциями клиентов, которые связаны с контекстом представления.</span><span class="sxs-lookup"><span data-stu-id="a8025-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="a8025-127">Например, контекст представления включается в активацию следующего или предыдущего сообщения, сортировку содержимого папки и фильтрацию содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="a8025-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="a8025-128">Не важно, какой механизм вы предоставляете пользователям для активации этих функций, важно только, чтобы семантика этих функций хорошо соотносима с методами в интерфейсе **IMAPIViewContext.**</span><span class="sxs-lookup"><span data-stu-id="a8025-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="a8025-129">Представление советовать раковина является объектом, который реализует [интерфейс IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) и обрабатывает уведомления с серверов форм, которые влияют на вашего зрителя и помочь формам и форме зрителей для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="a8025-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="a8025-130">Дополнительные сведения см. в [рублях Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="a8025-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

