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
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="cd1ba-103">Отправка сообщений с помощью MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1ba-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="cd1ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd1ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd1ba-105">Клиентские приложения вызывают [метод IMessage::SubmitMessage](imessage-submitmessage.md) для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="cd1ba-106">**SubmitMessage** вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы сохранить сообщение перед передачей управления в пулер MAPI или непосредственно поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="cd1ba-107">Пулер MAPI получает сообщение, если происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="cd1ba-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="cd1ba-108">Поставщик и поставщик транспорта, хранимые в хранилище сообщений, не имеют тесной связи.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="cd1ba-109">Сообщение требует предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="cd1ba-110">Тесное хранилище сообщений и транспорт не могут обрабатывать всех получателей, которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="cd1ba-111">Для загрузки сообщения поставщику транспорта в тесном хранилище сообщений необходимо учесть состояние сообщения, прежде чем оно будет представлено в пуле MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="cd1ba-112">В ряде ситуаций может показаться, что для сообщения требуется пулер MAPI, но в самом деле, это не должно быть задействовано.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="cd1ba-113">Например, рассмотрим ситуацию, когда пользователь передает сообщение из "Входящие".</span><span class="sxs-lookup"><span data-stu-id="cd1ba-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="cd1ba-114">Клиент использует тесное хранилище и транспорт.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="cd1ba-115">Если в тесном хранилище сообщений в качестве единственного критерия для принятия решения о том, следует ли разрешить пуле MAPI обрабатывать сообщение, то пулер MAPI всегда будет получать сообщение.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="cd1ba-116">Чтобы избежать подобных проблем, в тесном хранилище сообщений необходимо проверять состояние сообщения в дополнение к расположению сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="cd1ba-117">В частности, поставщик транспорта не должен запрашивать загрузку пулом MAPI сообщений, которые активно отправлены.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="cd1ba-118">Процесс передачи сообщений включает поставщика хранения сообщений, одного или несколько поставщиков транспорта и MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="cd1ba-119">В темах этого раздела подробно описаны определенные роли в процессе передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd1ba-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cd1ba-120">See also</span></span>



[<span data-ttu-id="cd1ba-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cd1ba-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="cd1ba-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="cd1ba-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

