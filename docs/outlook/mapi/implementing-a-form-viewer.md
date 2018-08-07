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
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809282"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="f8065-103">Реализация средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="f8065-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="f8065-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8065-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8065-105">Форма просмотра включает в себя три объекта: сайте сообщение представления уведомить приемник и контекста представления.</span><span class="sxs-lookup"><span data-stu-id="f8065-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="f8065-106">Каждый из этих объектов позволяет взаимодействовать с сервером в форме и ее формы.</span><span class="sxs-lookup"><span data-stu-id="f8065-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="f8065-107">Сообщение сайта — это объект, реализующий [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) интерфейс, а также приводятся сведения, серверы формы с помощью задач, таких как перемещение, сохранение, удаление сообщений, создание новых сообщений или запуск новые серверы формы.</span><span class="sxs-lookup"><span data-stu-id="f8065-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="f8065-108">Сайты сообщения используются для получения сведений о состоянии вашего клиента по отношению к различных поставщиков услуг с форм.</span><span class="sxs-lookup"><span data-stu-id="f8065-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="f8065-109">К примеру формы можно использовать веб-узла сообщения для получения указателя на текущий хранения сообщений, сообщение или папку.</span><span class="sxs-lookup"><span data-stu-id="f8065-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="f8065-110">Существует два типа методов в интерфейсе **IMAPIMessageSite** .</span><span class="sxs-lookup"><span data-stu-id="f8065-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="f8065-111">Методы, которые содержатся сведения, которые объектам формы.</span><span class="sxs-lookup"><span data-stu-id="f8065-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="f8065-112">Методы для обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8065-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="f8065-113">Методы, которые содержатся сведения, которые объекты формы, просты в использовании.</span><span class="sxs-lookup"><span data-stu-id="f8065-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="f8065-114">Кроме случаев, когда [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), необходимо иметь доступные сведения, необходимые для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="f8065-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="f8065-115">Методы, работа с элементами управления сообщения должен работать, как если было запущено через регулярные пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f8065-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="f8065-116">Например если объект формы вызывает метод [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , функционируют как пользователь выбрал для создания нового настраиваемого сообщения с регулярным пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f8065-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="f8065-117">Команды, которые обычно создают это поведение, **создания**, **Open**, **Ответить**, **Ответить всем получателям**и **вперед**.</span><span class="sxs-lookup"><span data-stu-id="f8065-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="f8065-118">Контекст представления — это объект, реализующий [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) интерфейс, а также предоставляет серверы формы с контекстом для текущего сообщения, позволяя серверы для простоты перехода к следующему или предыдущему сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="f8065-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="f8065-119">Режим контекст представления для общего доступа к информации.</span><span class="sxs-lookup"><span data-stu-id="f8065-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="f8065-120">Объект context представления формы выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f8065-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="f8065-121">Зарегистрируйте клиента для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f8065-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="f8065-122">Активируйте следующий или предыдущий сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="f8065-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="f8065-123">Получите сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="f8065-123">Get printing information.</span></span>
    
- <span data-ttu-id="f8065-124">Получите сведения о состоянии вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="f8065-124">Get your client's status.</span></span>
    
- <span data-ttu-id="f8065-125">Получите поток, который можно использовать для сохранения текстовая версия сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8065-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="f8065-126">Же, как в [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) интерфейс, методы в **IMAPIViewContext** их с помощью пользовательских действий и настройку клиентских функций, имеющих отношение к контекст представления.</span><span class="sxs-lookup"><span data-stu-id="f8065-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="f8065-127">Например контекст представления, связанного с Активация сообщения следующий или предыдущий, содержимое папки Сортировка и фильтрация содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="f8065-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="f8065-128">Не имеет значения по механизму предоставляют для пользователей, чтобы активировать эти функции, важно только что семантика этих функций сопоставляются со методов в интерфейсе **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="f8065-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="f8065-129">Представление уведомить приемник объект, реализующий [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) интерфейс и значками уведомлений с серверов формы, влияющие на формах просмотра и справки и средства просмотра формы для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="f8065-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="f8065-130">Для получения дополнительных сведений см [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f8065-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

