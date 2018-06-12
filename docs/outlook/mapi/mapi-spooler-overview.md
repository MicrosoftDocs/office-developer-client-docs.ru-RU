---
title: Обзор диспетчера очереди MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809845"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="ebdb0-103">Обзор диспетчера очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="ebdb0-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="ebdb0-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebdb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebdb0-105">Диспетчер очереди MAPI — это функция Microsoft Office Outlook процесс, отвечающий за отправку сообщений в и получение сообщений из систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="ebdb0-106">Диспетчер очереди MAPI играет важнейшую роль в сообщении и доставки.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="ebdb0-107">При недоступности системы обмена сообщениями, диспетчер очереди MAPI хранятся сообщения и автоматически пересылает их в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="ebdb0-108">Эта возможность содержатся на в или отправки данных в случае необходимости называется хранения и пересылки, критическим компонентом в средах, где удаленные подключения общих и сетевого трафика высокой.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="ebdb0-109">Диспетчер очереди MAPI работает как в фоновом потоке в Outlook.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="ebdb0-110">Диспетчер очереди MAPI имеет дополнительные обязанности, связанные с рассылки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="ebdb0-111">Эти дополнительные операции относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="ebdb0-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="ebdb0-112">Позволяет отслеживать их типы получателей, которые обрабатываются поставщиков определенного транспорта.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="ebdb0-113">Время доставки новое сообщение, уведомляющее о клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="ebdb0-114">Предварительная обработка и последующая обработка вызова сообщение.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="ebdb0-115">Создание отчетов, которые указывают, доставки сообщения произошла.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="ebdb0-116">Поддержка состояния на обработанные получателей.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="ebdb0-117">На следующем рисунке показана на высоком уровне потоки сообщение от клиента к системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="ebdb0-118">**Поток обработки исходящих сообщений**</span><span class="sxs-lookup"><span data-stu-id="ebdb0-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="ebdb0-119">![Исходящий поток сообщений] (media/amapi_46.gif "Исходящий поток сообщений")</span><span class="sxs-lookup"><span data-stu-id="ebdb0-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="ebdb0-120">Пользователь клиентское приложение отправляет сообщение для одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="ebdb0-121">Сообщение хранилища поставщика инициирует процесс отправки форматирования сообщения с Дополнительные сведения, необходимые для передачи.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="ebdb0-122">Диспетчер очереди MAPI получает сообщение для обработки при возникновении любого из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="ebdb0-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="ebdb0-123">Поставщик хранения сообщения не является тесно связанным с помощью поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="ebdb0-124">Сообщение необходимо предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="ebdb0-125">Хранение сообщений и транспорта тесно поставщика, но они не могут обрабатывать всех получателей, которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="ebdb0-126">Если диспетчер очереди MAPI получает сообщение, выполняет все необходимые предварительной обработки и доставляет сообщение в поставщике соответствующий транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="ebdb0-127">Поставщик транспорта обеспечивает сообщение к его систем обмена сообщениями, который отправляет его получателю.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="ebdb0-128">С помощью входящих сообщений потока изменен на обратный.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="ebdb0-129">Поставщика транспорта получает сообщение из его систем обмена сообщениями и уведомляет диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="ebdb0-130">Очереди выполняет все необходимые постобработку и информирует поставщика хранилища сообщений, что пришло новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="ebdb0-131">Это уведомление вызывает клиента, чтобы обновить его отображение сообщений, позволяя пользователям для чтения нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="ebdb0-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebdb0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ebdb0-132">See also</span></span>

- [<span data-ttu-id="ebdb0-133">Функции MAPI и архитектура</span><span class="sxs-lookup"><span data-stu-id="ebdb0-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

