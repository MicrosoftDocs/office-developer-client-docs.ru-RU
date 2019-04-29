---
title: Реализация средства просмотра форм
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
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="7ba43-103">Реализация средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="7ba43-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="7ba43-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ba43-105">Средство просмотра форм включает три объекта: сайт сообщений, приемник уведомлений о представлении и контекст представления.</span><span class="sxs-lookup"><span data-stu-id="7ba43-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="7ba43-106">Каждый из этих объектов позволяет взаимодействовать с сервером форм и формами.</span><span class="sxs-lookup"><span data-stu-id="7ba43-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="7ba43-107">Сайт сообщения — это объект, который реализует интерфейс [имапимессажесите: IUnknown](imapimessagesiteiunknown.md) и помогает серверам форм создавать такие задачи, как перемещение, сохранение или удаление сообщений, создание новых сообщений или запуск новых серверов форм.</span><span class="sxs-lookup"><span data-stu-id="7ba43-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="7ba43-108">Сайты сообщений используются формами для получения сведений о состоянии клиента по отношению к различным поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="7ba43-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="7ba43-109">Например, форма может использовать ваш сайт сообщений для получения указателя на текущее хранилище сообщений, сообщение или папку.</span><span class="sxs-lookup"><span data-stu-id="7ba43-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="7ba43-110">В интерфейсе **Имапимессажесите** существует два типа методов:</span><span class="sxs-lookup"><span data-stu-id="7ba43-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="7ba43-111">Методы, предоставляющие сведения для объектов Form.</span><span class="sxs-lookup"><span data-stu-id="7ba43-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="7ba43-112">Методы, управляющие сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7ba43-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="7ba43-113">Методы, которые предоставляют сведения для объектов формы, просты для реализации.</span><span class="sxs-lookup"><span data-stu-id="7ba43-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="7ba43-114">Во всех случаях, кроме [имапимессажесите:: жетситестатус](imapimessagesite-getsitestatus.md), у вас уже должны быть сведения, необходимые для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="7ba43-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="7ba43-115">Методы, управляющие сообщениями, должны действовать так, как если бы они были активированы с помощью обычного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7ba43-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="7ba43-116">Например, если объект Form вызывает метод [имапимессажесите:: невмессаже](imapimessagesite-newmessage.md) , то будет действовать так, как если бы пользователь выбрал создание нового настраиваемого сообщения с обычным пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="7ba43-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="7ba43-117">Как правило, в этом случае создаются такие команды, как **Создание**, **Открытие**, **ответ**, **ответ всем получателям**и пересылка. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7ba43-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="7ba43-118">Контекст представления — это объект, который реализует интерфейс [имапивиевконтекст: IUnknown](imapiviewcontextiunknown.md) и предоставляет серверы форм с контекстом для текущего сообщения, позволяя серверам легко переходить к следующему или предыдущему сообщению в папке.</span><span class="sxs-lookup"><span data-stu-id="7ba43-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="7ba43-119">Для обмена сведениями В форме используется контекст представления.</span><span class="sxs-lookup"><span data-stu-id="7ba43-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="7ba43-120">С помощью объекта контекста представления форма может:</span><span class="sxs-lookup"><span data-stu-id="7ba43-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="7ba43-121">Регистрация у клиента для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7ba43-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="7ba43-122">Активация следующего или предыдущего сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="7ba43-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="7ba43-123">Получение сведений о печати.</span><span class="sxs-lookup"><span data-stu-id="7ba43-123">Get printing information.</span></span>
    
- <span data-ttu-id="7ba43-124">Получение состояния клиента.</span><span class="sxs-lookup"><span data-stu-id="7ba43-124">Get your client's status.</span></span>
    
- <span data-ttu-id="7ba43-125">Получение потока, который можно использовать для сохранения текстовой версии сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ba43-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="7ba43-126">Аналогично методам в интерфейсе [имапимессажесите: IUnknown](imapimessagesiteiunknown.md) методы в **имапивиевконтекст** сопоставляются с действиями пользователя и клиентскими функциями, которые относятся к контексту представления.</span><span class="sxs-lookup"><span data-stu-id="7ba43-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="7ba43-127">Например, контекст представления включает активацию следующего или предыдущего сообщения, сортировку содержимого папки и фильтрацию содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="7ba43-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="7ba43-128">Не важно, какой механизм вы предоставляете пользователям для активации этих функций, поэтому важно, чтобы семантика этих функций хорошо сопоставлена с методами в интерфейсе **имапивиевконтекст** .</span><span class="sxs-lookup"><span data-stu-id="7ba43-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="7ba43-129">Приемник рекомендаций по просмотру — это объект, который реализует интерфейс [имапивиевадвисесинк: IUnknown](imapiviewadvisesinkiunknown.md) и обрабатывает уведомления от серверов форм, которые влияют на средство просмотра и формы справки и средства просмотра форм для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="7ba43-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="7ba43-130">Дополнительную информацию можно узнать в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7ba43-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

