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
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412417"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="2106c-103">Загрузка сообщения в форму</span><span class="sxs-lookup"><span data-stu-id="2106c-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="2106c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2106c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2106c-105">Чтобы загрузить существующее сообщение в форму с помощью сервера форм, используйте одну из следующих стратегий.</span><span class="sxs-lookup"><span data-stu-id="2106c-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="2106c-106">Call [IMAPISession::P репареформ](imapisession-prepareform.md) для создания маркера, а затем [IMAPISession:: шовформ](imapisession-showform.md) для отображения формы.</span><span class="sxs-lookup"><span data-stu-id="2106c-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="2106c-107">Call [имапиформмгр:: лоадформ](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="2106c-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="2106c-108">Использование стратегии **препареформ** и **шовформ** сравнительно упрощается, но это приводит к отображению форм, которые являются модальными по отношению к вашему клиенту.</span><span class="sxs-lookup"><span data-stu-id="2106c-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="2106c-109">Это вызвано тем, что вызов **шовформ** не возвращается, пока форма не будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="2106c-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="2106c-110">Если вам требуется асинхронная обработка форм, не используйте эту стратегию.</span><span class="sxs-lookup"><span data-stu-id="2106c-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="2106c-111">Использование стратегии **лоадформ** усложняется, так как метод требует несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="2106c-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="2106c-112">Эти параметры указывают диспетчеру форм на необходимость запуска соответствующего сервера форм в правильном контексте и отображения соответствующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="2106c-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="2106c-113">Если сервер форм уже запущен, Диспетчер форм загружает сообщение на сервер форм без запуска нового экземпляра сервера форм.</span><span class="sxs-lookup"><span data-stu-id="2106c-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="2106c-114">Чтобы указать, какой сервер формы необходимо запустить, передайте класс сообщения, обрабатываемый целевым сервером, в содержимое параметра _лпсзмессажекласс_ .</span><span class="sxs-lookup"><span data-stu-id="2106c-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="2106c-115">Соответствующий класс сообщения можно определить, получив свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения, которое необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="2106c-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="2106c-116">Иногда для указанного класса сообщений отсутствует сервер форм, а только сервер форм, который обрабатывает сообщения, принадлежащие суперклассу этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2106c-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="2106c-117">Если вы хотите, чтобы сообщение загружалось только сервером форм, специально предназначенным для обработки сообщений этого класса, установите флаг МАПИФОРМ_ЕКСАКТМАТЧ в вызове **лоадформ** .</span><span class="sxs-lookup"><span data-stu-id="2106c-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="2106c-118">Дополнительные сведения см. [](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="2106c-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="2106c-119">**Лоадформ** также требует указатель на сайт сообщений и контекст представления средства просмотра и значение **пр_мсг_статус** целевого сообщения ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) и **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). параметры.</span><span class="sxs-lookup"><span data-stu-id="2106c-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

