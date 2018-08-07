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
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809755"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="efbee-103">Общие сведения о формах MAPI</span><span class="sxs-lookup"><span data-stu-id="efbee-103">MAPI forms overview</span></span>
  
<span data-ttu-id="efbee-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efbee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efbee-105">Формы MAPI — это средство просмотра для сообщения.</span><span class="sxs-lookup"><span data-stu-id="efbee-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="efbee-106">Каждое сообщение имеет класс сообщений, который определяет определенной формы, которая используется в качестве его просмотра.</span><span class="sxs-lookup"><span data-stu-id="efbee-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="efbee-107">MAPI определяет несколько классов сообщений и производитель реализовал формы для просмотра сообщений из этих классов.</span><span class="sxs-lookup"><span data-stu-id="efbee-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="efbee-108">Разработчики клиентских приложений можно создать новые классы сообщений и настраиваемые формы для просмотра сообщений, созданных с помощью новых классов.</span><span class="sxs-lookup"><span data-stu-id="efbee-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="efbee-109">Каждые настраиваемая форма реализует набор стандартных команд меню, такие как **Open**, **Создание**, **Удаление**и **ответ**и набор команд, которые специфичны для определенной формы.</span><span class="sxs-lookup"><span data-stu-id="efbee-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="efbee-110">Некоторые команды формы интегрированы с пользовательским интерфейсом в клиентском приложении, если форма активна; другие команды формы полностью заменить команды клиента.</span><span class="sxs-lookup"><span data-stu-id="efbee-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="efbee-111">На следующем рисунке показана связь между компонентами MAPI, связанные с использованием форм.</span><span class="sxs-lookup"><span data-stu-id="efbee-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="efbee-112">**Архитектура формы MAPI**</span><span class="sxs-lookup"><span data-stu-id="efbee-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="efbee-113">![Архитектура формы MAPI] (media/forms01.gif "Архитектура формы MAPI")</span><span class="sxs-lookup"><span data-stu-id="efbee-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="efbee-114">На схеме Обратите внимание на то, что диспетчер форм играет роль, похожие на других поставщиков служб MAPI, хотя это не самого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="efbee-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="efbee-115">Диспетчер форм — заменяемый DLL-Библиотеку, который реализует некоторые интерфейсы MAPI.</span><span class="sxs-lookup"><span data-stu-id="efbee-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="efbee-116">Несмотря на то, что разработчики могут реализовать собственные диспетчер форм, большинство сред будет использовать диспетчер форм, предоставляемым корпорацией Майкрософт из-за сложности диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="efbee-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="efbee-117">В следующем списке описываются компоненты в схему и их связи с другими компонентами:</span><span class="sxs-lookup"><span data-stu-id="efbee-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="efbee-118">Клиент обмена сообщениями: приложение, которое можно использовать объекты формы.</span><span class="sxs-lookup"><span data-stu-id="efbee-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="efbee-119">Клиент обмена мгновенными сообщениями использует интерфейсы формы MAPI для связи с диспетчер форм для загрузки сообщения в виде объектов.</span><span class="sxs-lookup"><span data-stu-id="efbee-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="efbee-120">Интерфейсы формы MAPI: определенный стандарт для взаимодействия между компонентами MAPI, которые связаны с форм.</span><span class="sxs-lookup"><span data-stu-id="efbee-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="efbee-121">Диспетчер форм: DLL, обмена мгновенными сообщениями клиенты будут использовать для обработки установки формы в библиотеки форм, загрузки формы серверов и начальной связи между обмена сообщениями клиентов и серверов формы.</span><span class="sxs-lookup"><span data-stu-id="efbee-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="efbee-122">Библиотеки форм: постоянное хранилище для исполняемых файлов, связанных с серверами формы.</span><span class="sxs-lookup"><span data-stu-id="efbee-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="efbee-123">Форма серверы: исполняемые файлы, которые реализуют формы.</span><span class="sxs-lookup"><span data-stu-id="efbee-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="efbee-124">Серверы формы создания объектов формы и пользовательских интерфейсов для работы с определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="efbee-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="efbee-125">Этот исполняемый файл также является сервером OLE и соответствующий обычными соглашениями OLE.</span><span class="sxs-lookup"><span data-stu-id="efbee-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="efbee-126">Форма объектов: объекты во время выполнения, созданные формы серверы, которые соответствуют конкретные сообщения.</span><span class="sxs-lookup"><span data-stu-id="efbee-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="efbee-127">Объекты формы выполняются в контексте процесса их сервера форм.</span><span class="sxs-lookup"><span data-stu-id="efbee-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="efbee-128">Дополнительные сведения о компонентах формы MAPI просмотрите [Формы MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="efbee-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efbee-129">См. также</span><span class="sxs-lookup"><span data-stu-id="efbee-129">See also</span></span>

- [<span data-ttu-id="efbee-130">Функции MAPI и архитектура</span><span class="sxs-lookup"><span data-stu-id="efbee-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

