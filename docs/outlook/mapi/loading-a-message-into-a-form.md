---
title: Загрузка сообщения в форму
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576500"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="9d54d-103">Загрузка сообщения в форму</span><span class="sxs-lookup"><span data-stu-id="9d54d-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="9d54d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d54d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d54d-105">Чтобы загрузить существующее сообщение в форму с помощью сервера форм, используйте одну из следующих стратегий.</span><span class="sxs-lookup"><span data-stu-id="9d54d-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="9d54d-106">Вызов [IMAPISession::PrepareForm](imapisession-prepareform.md) для создания маркера и затем [IMAPISession::ShowForm](imapisession-showform.md) для отображения формы.</span><span class="sxs-lookup"><span data-stu-id="9d54d-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="9d54d-107">Вызов [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="9d54d-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="9d54d-108">С помощью стратегии **PrepareForm** и **ShowForm** сравнительно легко, но результаты в формах, которые являются модальными по отношению к вашей клиента.</span><span class="sxs-lookup"><span data-stu-id="9d54d-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="9d54d-109">Это вызов **ShowForm** не возвращает пока выйдет из формы.</span><span class="sxs-lookup"><span data-stu-id="9d54d-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="9d54d-110">Если вам требуется для обработки форм асинхронно, не используйте этой стратегии.</span><span class="sxs-lookup"><span data-stu-id="9d54d-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="9d54d-111">С помощью стратегии **LoadForm** сложнее, так как метод требует несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="9d54d-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="9d54d-112">Эти параметры диспетчеру формы для запуска сервера соответствующую форму в контексте соответствующих прав и отображения соответствующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d54d-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="9d54d-113">Если на сервере формы уже выполняется, диспетчер форм загружает сообщения в сервера форм без запуска нового экземпляра сервера формы.</span><span class="sxs-lookup"><span data-stu-id="9d54d-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="9d54d-114">Чтобы указать, какой сервер формы для запуска, передайте класс сообщения, обрабатываемых на целевой сервер в содержимое параметра _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="9d54d-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="9d54d-115">Класс соответствующего сообщения можно определить извлекая свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения для загрузки.</span><span class="sxs-lookup"><span data-stu-id="9d54d-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="9d54d-116">В некоторых случаях нет ни одного сервера формы для указанного класса сообщений, только сервер формы, который обрабатывает сообщения, относящегося к суперкласса сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d54d-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="9d54d-117">Ниже приведена загрузку сообщений только с сервера форм, специально предназначенный для обработки сообщений этого класса, задайте флаг MAPIFORM_EXACTMATCH в вызове **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="9d54d-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="9d54d-118">Для получения дополнительных сведений см [Классы сообщений MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9d54d-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="9d54d-119">**LoadForm** также требуется указатель сайта вашей средства просмотра сообщений и контекст представления и значение для сообщения целевой **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) и **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) свойства.</span><span class="sxs-lookup"><span data-stu-id="9d54d-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

