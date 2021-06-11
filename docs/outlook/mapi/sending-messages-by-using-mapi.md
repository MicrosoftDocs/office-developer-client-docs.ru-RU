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
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438724"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="be42e-103">Отправка сообщений с помощью MAPI</span><span class="sxs-lookup"><span data-stu-id="be42e-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="be42e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be42e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be42e-105">Клиентские приложения звонят [по методу IMessage::SubmitMessage](imessage-submitmessage.md) для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="be42e-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="be42e-106">**SubmitMessage** вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы сохранить сообщение перед передачей управления в пулер MAPI или непосредственно поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="be42e-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="be42e-107">Spooler MAPI получает сообщение, если произойдет следующее:</span><span class="sxs-lookup"><span data-stu-id="be42e-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="be42e-108">Поставщик и поставщик транспорта для хранения сообщений не тесно совмещение.</span><span class="sxs-lookup"><span data-stu-id="be42e-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="be42e-109">Сообщение требует предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="be42e-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="be42e-110">Тесное хранилище и транспорт сообщений не может обрабатывать всех получателей, к которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="be42e-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="be42e-111">В тесном хранилище сообщений необходимо принять во внимание состояние сообщения, прежде чем оно будет представлено в пулер MAPI, который будет загружен поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="be42e-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="be42e-112">Существуют ситуации, когда сообщение может потребовать пульпера MAPI, но шпалер MAPI действительно не должен быть вовлечен.</span><span class="sxs-lookup"><span data-stu-id="be42e-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="be42e-113">Например, рассмотрим ситуацию, когда пользователь передает сообщение из почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="be42e-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="be42e-114">Клиент использует тесно соединый магазин и транспорт.</span><span class="sxs-lookup"><span data-stu-id="be42e-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="be42e-115">Если в тесном хранилище сообщений используется расположение сообщения в качестве единственного критерия для принятия решения о том, разрешить ли пуллеру MAPI обрабатывать сообщение, пуллер MAPI всегда будет получать сообщение.</span><span class="sxs-lookup"><span data-stu-id="be42e-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="be42e-116">Чтобы избежать подобных проблем, в хранилище сообщений с тесной связи необходимо проверить состояние сообщения в дополнение к расположению сообщения.</span><span class="sxs-lookup"><span data-stu-id="be42e-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="be42e-117">В частности, поставщик транспорта не должен запрашивать, чтобы spooler MAPI скачал любое сообщение, которое активно отправлено.</span><span class="sxs-lookup"><span data-stu-id="be42e-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="be42e-118">Процесс передачи сообщений включает поставщика хранения сообщений, одного или несколько поставщиков транспорта и MAPI.</span><span class="sxs-lookup"><span data-stu-id="be42e-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="be42e-119">В разделах этого раздела подробно описаны конкретные роли в процессе передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="be42e-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be42e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="be42e-120">See also</span></span>



[<span data-ttu-id="be42e-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="be42e-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="be42e-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="be42e-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

