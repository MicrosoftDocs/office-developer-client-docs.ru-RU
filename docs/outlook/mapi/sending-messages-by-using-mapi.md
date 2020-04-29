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
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="411fa-103">Отправка сообщений с помощью MAPI</span><span class="sxs-lookup"><span data-stu-id="411fa-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="411fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="411fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="411fa-105">Клиентские приложения вызывают метод [iMessage:: субмитмессаже](imessage-submitmessage.md) для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="411fa-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="411fa-106">**Субмитмессаже** вызывает [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для сохранения сообщения перед передачей управления диспетчеру MAPI или непосредственно поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="411fa-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="411fa-107">Очередь MAPI получает сообщение в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="411fa-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="411fa-108">Поставщик хранилища сообщений и поставщик транспорта не тесно связаны.</span><span class="sxs-lookup"><span data-stu-id="411fa-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="411fa-109">Сообщение требует предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="411fa-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="411fa-110">Тесно связанный банк сообщений и транспорт не могут обрабатывать всех получателей, которым адресовано сообщение.</span><span class="sxs-lookup"><span data-stu-id="411fa-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="411fa-111">Жестко связанное хранилище сообщений должно учитывать состояние сообщения перед тем, как оно будет представлено диспетчером очереди MAPI для загрузки в поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="411fa-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="411fa-112">Существуют ситуации, в которых может потребоваться, чтобы в сообщении отображался почтовый диспетчер MAPI, но диспетчер очереди MAPI не должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="411fa-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="411fa-113">Например, рассмотрим ситуацию, когда пользователь передает сообщение из папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="411fa-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="411fa-114">Клиент использует тесно связанное хранилище и транспорт.</span><span class="sxs-lookup"><span data-stu-id="411fa-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="411fa-115">Если тесно связанное хранилище сообщений использует расположение сообщения в качестве единственного условия для принятия решения о том, следует ли разрешить диспетчеру очереди MAPI обрабатывать сообщение, диспетчер очереди MAPI всегда будет получать сообщение.</span><span class="sxs-lookup"><span data-stu-id="411fa-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="411fa-116">Чтобы избежать такого рода проблем, строго связанное хранилище сообщений должно проверять состояние сообщения в дополнение к расположению сообщения.</span><span class="sxs-lookup"><span data-stu-id="411fa-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="411fa-117">В частности, поставщик транспорта не должен запрашивать, чтобы диспетчер очереди MAPI загружал сообщение, которое отправляется в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="411fa-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="411fa-118">Процесс передачи сообщений включает в себя поставщика хранилища сообщений, одного или нескольких поставщиков транспорта и MAPI.</span><span class="sxs-lookup"><span data-stu-id="411fa-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="411fa-119">В подразделах этого раздела представлены подробные сведения об определенных ролях в процессе передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="411fa-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="411fa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="411fa-120">See also</span></span>



[<span data-ttu-id="411fa-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="411fa-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="411fa-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="411fa-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

