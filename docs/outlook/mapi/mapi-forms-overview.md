---
title: Общие сведения о формах MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432522"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="d549c-103">Общие сведения о формах MAPI</span><span class="sxs-lookup"><span data-stu-id="d549c-103">MAPI forms overview</span></span>
  
<span data-ttu-id="d549c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d549c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d549c-105">Форма MAPI — это средство просмотра сообщения.</span><span class="sxs-lookup"><span data-stu-id="d549c-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="d549c-106">Каждое сообщение имеет класс Message, который определяет конкретную форму, используемую в качестве средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="d549c-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="d549c-107">MAPI определяет несколько классов сообщений и реализует формы для просмотра сообщений этих классов.</span><span class="sxs-lookup"><span data-stu-id="d549c-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="d549c-108">Разработчики клиентского программного обеспечения могут создавать новые классы сообщений и настраиваемые формы для просмотра сообщений, созданных с помощью новых классов.</span><span class="sxs-lookup"><span data-stu-id="d549c-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="d549c-109">Каждая настраиваемая форма реализует набор стандартных команд меню, таких как **Открытие**, **Создание**, **Удаление**и **ответ**, а также набор команд, характерных для конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="d549c-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="d549c-110">Некоторые команды формы интегрированы с пользовательским интерфейсом клиентского приложения, если форма активна; другие команды формы полностью заменяют клиентские команды.</span><span class="sxs-lookup"><span data-stu-id="d549c-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="d549c-111">На следующем рисунке показана связь между компонентами MAPI, которые используются в формах.</span><span class="sxs-lookup"><span data-stu-id="d549c-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="d549c-112">**Архитектура формы MAPI**</span><span class="sxs-lookup"><span data-stu-id="d549c-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="d549c-113">![Архитектура форм MAPI] (media/forms01.gif "Архитектура форм MAPI")</span><span class="sxs-lookup"><span data-stu-id="d549c-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="d549c-114">Обратите внимание, что Диспетчер форм играет роль, похожую на другие поставщики службы MAPI, хотя это не сам поставщик службы.</span><span class="sxs-lookup"><span data-stu-id="d549c-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="d549c-115">Диспетчер форм — это заменяемая библиотека DLL, которая реализует некоторые интерфейсы MAPI.</span><span class="sxs-lookup"><span data-stu-id="d549c-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="d549c-116">Несмотря на то, что разработчики могут реализовать собственный диспетчер форм, большинство сред будет использовать Диспетчер форм, предоставляемый корпорацией Майкрософт, из-за сложности диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="d549c-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="d549c-117">В следующем списке описаны компоненты схемы и их связи с другими компонентами:</span><span class="sxs-lookup"><span data-stu-id="d549c-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="d549c-118">Клиент обмена сообщениями: приложение, которое может использовать объекты форм.</span><span class="sxs-lookup"><span data-stu-id="d549c-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="d549c-119">Клиент обмена сообщениями использует интерфейсы форм MAPI для обмена сообщениями с диспетчером форм, чтобы загружать сообщения в объекты формы.</span><span class="sxs-lookup"><span data-stu-id="d549c-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="d549c-120">Интерфейсы форм MAPI: определенный стандарт для обмена данными между компонентами MAPI, которые относятся к формам.</span><span class="sxs-lookup"><span data-stu-id="d549c-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="d549c-121">Диспетчер форм: Библиотека DLL, используемая клиентами для обмена сообщениями для обработки установки форм в библиотеках форм, загрузки серверов форм и начальной связи между клиентами обмена сообщениями и серверами форм.</span><span class="sxs-lookup"><span data-stu-id="d549c-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="d549c-122">Библиотеки форм: постоянное хранилище для исполняемых файлов, связанных с серверами форм.</span><span class="sxs-lookup"><span data-stu-id="d549c-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="d549c-123">Серверы форм: исполняемые файлы, реализующие форму.</span><span class="sxs-lookup"><span data-stu-id="d549c-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="d549c-124">Серверы форм создают объекты форм и пользовательские интерфейсы для работы с определенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d549c-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="d549c-125">Этот исполняемый файл также является сервером OLE и соответствует обычным соглашениям OLE.</span><span class="sxs-lookup"><span data-stu-id="d549c-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="d549c-126">Объекты форм: объекты времени выполнения, созданные серверами форм, которые соответствуют определенным сообщениям.</span><span class="sxs-lookup"><span data-stu-id="d549c-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="d549c-127">Объекты формы выполняются в том же контексте процесса, что и сервер форм.</span><span class="sxs-lookup"><span data-stu-id="d549c-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="d549c-128">Дополнительные сведения о компонентах форм MAPI приведены в статье [MAPI Forms](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="d549c-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d549c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d549c-129">See also</span></span>

- [<span data-ttu-id="d549c-130">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="d549c-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

