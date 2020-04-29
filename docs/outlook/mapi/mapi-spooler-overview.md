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
# <a name="mapi-spooler-overview"></a><span data-ttu-id="f4e39-103">Общие сведения о системе буферизации MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e39-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="f4e39-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4e39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4e39-105">Диспетчер очереди MAPI является функцией процесса Microsoft Office Outlook, который отвечает за отправку и получение сообщений из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f4e39-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="f4e39-106">Диспетчер очереди MAPI играет важную роль в получении и доставке сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4e39-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="f4e39-107">Если система обмена сообщениями недоступна, диспетчер очереди MAPI сохраняет сообщения и автоматически пересылает их позже.</span><span class="sxs-lookup"><span data-stu-id="f4e39-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="f4e39-108">Эта возможность хранения или отправки данных, если это необходимо, называется хранением и пересылкой, важнейшим компонентом в средах, в которых удаленные подключения являются общими и высоким трафиком в сети.</span><span class="sxs-lookup"><span data-stu-id="f4e39-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="f4e39-109">Диспетчер очереди MAPI работает в качестве фонового потока в Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4e39-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="f4e39-110">Диспетчер очереди MAPI имеет дополнительные обязанности, связанные с распространением сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4e39-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="f4e39-111">К этим дополнительным пошлинам относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="f4e39-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="f4e39-112">Отслеживание типов получателей, которые обрабатываются определенными поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="f4e39-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="f4e39-113">Уведомление клиентского приложения о доставке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="f4e39-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="f4e39-114">Вызов предварительной обработки и обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4e39-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="f4e39-115">Создание отчетов, указывающих на то, что произошла доставка сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4e39-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="f4e39-116">Обслуживание состояния обработанных получателей.</span><span class="sxs-lookup"><span data-stu-id="f4e39-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="f4e39-117">На следующем рисунке показана высокая степень перепотока сообщений от клиента к системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f4e39-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="f4e39-118">**Поток обработки исходящих сообщений**</span><span class="sxs-lookup"><span data-stu-id="f4e39-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="f4e39-119">![Исходящий](media/amapi_46.gif "процесс") обработки исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="f4e39-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="f4e39-120">Пользователь клиентского приложения отправляет сообщение одному или нескольким получателям.</span><span class="sxs-lookup"><span data-stu-id="f4e39-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="f4e39-121">Поставщик хранилища сообщений начинает процесс отправки и форматирует сообщение с дополнительными сведениями, необходимыми для передачи.</span><span class="sxs-lookup"><span data-stu-id="f4e39-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="f4e39-122">Диспетчер очереди MAPI получает сообщение, которое обрабатывается, если выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="f4e39-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="f4e39-123">Поставщик хранилища сообщений не тесно связан с поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="f4e39-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="f4e39-124">Сообщение требует предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="f4e39-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="f4e39-125">Хранилище сообщений и поставщик транспорта тесно связаны, но они не могут обрабатывать всех получателей, которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4e39-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="f4e39-126">Если почтовый буфер MAPI получает сообщение, он выполняет необходимую предварительную обработку и доставляет сообщение соответствующему поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="f4e39-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="f4e39-127">Поставщик транспорта передает сообщение в систему обмена сообщениями, которое отправляет его предполагаемому получателю.</span><span class="sxs-lookup"><span data-stu-id="f4e39-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="f4e39-128">С входящими сообщениями этот процесс будет обратным.</span><span class="sxs-lookup"><span data-stu-id="f4e39-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="f4e39-129">Поставщик транспорта получает сообщение из системы обмена сообщениями и уведомляет Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4e39-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="f4e39-130">Диспетчер очереди выполняет все необходимые действия по обработке сообщений и информирует поставщика хранилища сообщений о том, что новое сообщение получено.</span><span class="sxs-lookup"><span data-stu-id="f4e39-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="f4e39-131">Это уведомление приводит к тому, что клиент обновляет отображение сообщения, позволяя пользователю прочитать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4e39-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4e39-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f4e39-132">See also</span></span>

- [<span data-ttu-id="f4e39-133">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e39-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

