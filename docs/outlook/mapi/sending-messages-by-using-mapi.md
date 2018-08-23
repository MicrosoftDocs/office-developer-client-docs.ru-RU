---
title: Отправка сообщений с помощью MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a3172dcd962c04d72aacd14d2e42990fb0f78c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593454"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="e72cb-103">Отправка сообщений с помощью MAPI</span><span class="sxs-lookup"><span data-stu-id="e72cb-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="e72cb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e72cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e72cb-105">Клиентские приложения вызовите метод [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="e72cb-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="e72cb-106">**SubmitMessage** вызывает [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для сохранения сообщения перед передачей управления диспетчер очереди MAPI или непосредственно к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="e72cb-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="e72cb-107">Диспетчер очереди MAPI получает сообщение при возникновении любого из следующих:</span><span class="sxs-lookup"><span data-stu-id="e72cb-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="e72cb-108">Поставщик транспорта и поставщика хранилища сообщений не являются тесно связанными.</span><span class="sxs-lookup"><span data-stu-id="e72cb-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="e72cb-109">Сообщение необходимо предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="e72cb-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="e72cb-110">Хранилище тесно связанных сообщений и транспорта не может обрабатывать всех получателей, которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="e72cb-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="e72cb-111">Хранилище тесно связанных сообщений следует учитывать состояние сообщения перед его представляет диспетчер очереди MAPI веб-сайта для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e72cb-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="e72cb-112">Бывают ситуации, чтобы сделать обязательным наличие диспетчер очереди MAPI может появиться сообщение, когда диспетчер очереди MAPI следует действительно не принимать участие.</span><span class="sxs-lookup"><span data-stu-id="e72cb-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="e72cb-113">Например рассмотрим ситуацию, когда пользователь отправляет сообщения, находящиеся в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e72cb-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="e72cb-114">Клиент использует тесно связанных хранилище и транспорта.</span><span class="sxs-lookup"><span data-stu-id="e72cb-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="e72cb-115">Если хранилище тесно связанных сообщений использует расположение сообщения в качестве единственного критерии решения о необходимости разрешить диспетчер очереди MAPI для обработки сообщения, диспетчер очереди MAPI всегда будет выведено сообщение.</span><span class="sxs-lookup"><span data-stu-id="e72cb-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="e72cb-116">Во избежание такой проблемы, хранилищем тесно связанных сообщений необходимо проверить состояние сообщения в дополнение к расположение сообщения.</span><span class="sxs-lookup"><span data-stu-id="e72cb-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="e72cb-117">В частности поставщика транспорта не должен запрашивать, что диспетчер очереди MAPI загрузите все сообщение, отправляемое активно.</span><span class="sxs-lookup"><span data-stu-id="e72cb-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="e72cb-118">Процесс передачи сообщений включает поставщика хранилища сообщений, одним или несколькими поставщиками транспорта и MAPI.</span><span class="sxs-lookup"><span data-stu-id="e72cb-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="e72cb-119">В этом разделе представлены подробные сведения о конкретных ролей в процессе передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="e72cb-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e72cb-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e72cb-120">See also</span></span>



[<span data-ttu-id="e72cb-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e72cb-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e72cb-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e72cb-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

