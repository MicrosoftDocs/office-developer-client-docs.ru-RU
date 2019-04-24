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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351452"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="30b4d-103">Диспетчер форм MAPI</span><span class="sxs-lookup"><span data-stu-id="30b4d-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="30b4d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30b4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30b4d-105">Диспетчер форм — это объект, который реализует интерфейс [имапиформмгр](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="30b4d-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="30b4d-106">Большинство организаций будут использовать Диспетчер форм, поставляемый с MAPI, который называется диспетчером форм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30b4d-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="30b4d-107">Однако при необходимости организация может заменить Диспетчер форм по умолчанию настраиваемым диспетчером форм.</span><span class="sxs-lookup"><span data-stu-id="30b4d-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="30b4d-108">Диспетчер форм выполняет поиск форм в библиотеках форм, загружает формы в ответ на запросы пользователей и устанавливает формы в локальную библиотеку форм, библиотеку форм папки или библиотеку личных форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="30b4d-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="30b4d-109">Чтобы пользователь мог взаимодействовать с сообщением, необходимо создать экземпляр сервера форм для класса сообщений сообщения и активировать его для отображения сообщения и выполнения запрошенной операции над сообщением.</span><span class="sxs-lookup"><span data-stu-id="30b4d-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="30b4d-110">Как описано в разделе [библиотеки форм MAPI](mapi-form-libraries.md), реализация формы может находиться в нескольких расположениях (библиотеках форм), а также нет гарантии того, что форма или ее сервер будут локально доступны или в состоянии выполнения, когда пользователь хочет взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="30b4d-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="30b4d-111">Диспетчер форм позаботится о том, как находить и активировать форму.</span><span class="sxs-lookup"><span data-stu-id="30b4d-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="30b4d-112">Клиенты используют службы, предоставляемые диспетчером форм, для поиска и активации форм.</span><span class="sxs-lookup"><span data-stu-id="30b4d-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="30b4d-113">Интерфейс **имапиформмгр** реализуется диспетчером форм и вызывается клиентами для доступа к службам.</span><span class="sxs-lookup"><span data-stu-id="30b4d-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="30b4d-114">Диспетчер форм является важнейшим компонентом, так как он скрывает практически все детали поиска и активации форм от клиентов обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="30b4d-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="30b4d-115">При загрузке серверов форм Диспетчер форм по умолчанию загружает форму из первой библиотеки форм, в которой находится реализация для класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="30b4d-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="30b4d-116">Диспетчер форм по умолчанию выполняет поиск в библиотеках форм в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="30b4d-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="30b4d-117">Локальная библиотека форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="30b4d-117">The user's local form library.</span></span> <span data-ttu-id="30b4d-118">Эта библиотека форм выполняет поиск в первую очередь, так как она обеспечивает самый быстрый доступ к реализации формы, если реализация установлена в локальной библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="30b4d-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="30b4d-119">Библиотека форм папки для контейнера сообщения — папка, в которой хранится загружаемое сообщение.</span><span class="sxs-lookup"><span data-stu-id="30b4d-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="30b4d-120">Личная библиотека форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="30b4d-120">The user's personal form library.</span></span>
    
<span data-ttu-id="30b4d-121">Настраиваемый диспетчер форм может выполнять поиск в доступных библиотеках форм в любом порядке или реализовывать другие библиотеки форм, такие как библиотека форм для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="30b4d-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="30b4d-122">Более подробную информацию о библиотеках форм можно узнать в статье [MAPI Forms Library](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="30b4d-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30b4d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="30b4d-123">See also</span></span>



[<span data-ttu-id="30b4d-124">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="30b4d-124">MAPI Forms</span></span>](mapi-forms.md)

