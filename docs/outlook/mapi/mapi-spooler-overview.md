---
title: Общие сведения о системе буферизации MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432718"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="938ee-103">Общие сведения о системе буферизации MAPI</span><span class="sxs-lookup"><span data-stu-id="938ee-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="938ee-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="938ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="938ee-105">Spooler MAPI — это функция процесса Microsoft Office Outlook, который отвечает за отправку сообщений и получение сообщений из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="938ee-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="938ee-106">Шпалер MAPI играет жизненно важную роль в получении и доставке сообщений.</span><span class="sxs-lookup"><span data-stu-id="938ee-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="938ee-107">Когда система обмена сообщениями недоступна, пульпер MAPI сохраняет сообщения и автоматически передает их в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="938ee-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="938ee-108">Эта возможность хранения или отправки данных при необходимости называется хранилищем и перенаправками, что является важной функцией в средах, где удаленные подключения являются общими, а сетевой трафик — высоким.</span><span class="sxs-lookup"><span data-stu-id="938ee-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="938ee-109">Шпалер MAPI выполняется в качестве фонового потока в Outlook.</span><span class="sxs-lookup"><span data-stu-id="938ee-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="938ee-110">У шпалеров MAPI есть дополнительные обязанности, связанные с распространением сообщений.</span><span class="sxs-lookup"><span data-stu-id="938ee-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="938ee-111">Эти дополнительные обязанности включают следующие:</span><span class="sxs-lookup"><span data-stu-id="938ee-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="938ee-112">Отслеживание типов получателей, которые обрабатываются конкретными поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="938ee-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="938ee-113">Информирование клиентского приложения при доставке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="938ee-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="938ee-114">Обращение к предварительной и постпроцессинговой подготовке сообщений.</span><span class="sxs-lookup"><span data-stu-id="938ee-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="938ee-115">Создание отчетов, которые указывают на то, что произошла доставка сообщений.</span><span class="sxs-lookup"><span data-stu-id="938ee-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="938ee-116">Сохранение состояния обрабатываемых получателей.</span><span class="sxs-lookup"><span data-stu-id="938ee-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="938ee-117">На следующем рисунке на высоком уровне показано, как сообщение перетекает из клиента в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="938ee-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="938ee-118">**Поток обработки исходящих сообщений**</span><span class="sxs-lookup"><span data-stu-id="938ee-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="938ee-119">![Исходяние потока исходяющих](media/amapi_46.gif "сообщений")</span><span class="sxs-lookup"><span data-stu-id="938ee-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="938ee-120">Пользователь клиентского приложения отправляет сообщение одному или более получателям.</span><span class="sxs-lookup"><span data-stu-id="938ee-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="938ee-121">Поставщик магазина сообщений инициирует процесс отправки, форматирование сообщения с помощью дополнительных сведений, необходимых для передачи.</span><span class="sxs-lookup"><span data-stu-id="938ee-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="938ee-122">Spooler MAPI получает сообщение для обработки, если возникает любое из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="938ee-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="938ee-123">Поставщик хранения сообщений не тесно совмещение с поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="938ee-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="938ee-124">Сообщение требует предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="938ee-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="938ee-125">Хранилище сообщений и поставщик транспорта тесно совмещение, но они не могут обрабатывать всех получателей, к которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="938ee-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="938ee-126">Если шпалер MAPI получает сообщение, он выполняет все необходимые препроцессы и передает сообщение соответствующему поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="938ee-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="938ee-127">Поставщик транспорта передает сообщение своей системе обмена сообщениями, которая отправляет его своему получателю.</span><span class="sxs-lookup"><span data-stu-id="938ee-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="938ee-128">При входящих сообщениях поток будет обратным.</span><span class="sxs-lookup"><span data-stu-id="938ee-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="938ee-129">Поставщик транспорта получает сообщение из своей системы обмена сообщениями и сообщает о spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="938ee-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="938ee-130">Spooler выполняет все необходимые постпроцессы и сообщает поставщику магазина сообщений о том, что пришло новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="938ee-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="938ee-131">Это уведомление заставляет клиента обновить отображение сообщений, что позволяет пользователю читать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="938ee-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="938ee-132">См. также</span><span class="sxs-lookup"><span data-stu-id="938ee-132">See also</span></span>

- [<span data-ttu-id="938ee-133">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="938ee-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

