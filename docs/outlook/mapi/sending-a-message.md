---
title: Отправка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590913"
---
# <a name="sending-a-message"></a><span data-ttu-id="eedec-103">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="eedec-103">Sending a Message</span></span>

  
  
<span data-ttu-id="eedec-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eedec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eedec-105">Когда вы готовы для отправки сообщения, вызове метода [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="eedec-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="eedec-106">**SubmitMessage** помещает его в очередь исходящих и устанавливает для флага MSGFLAG_SUBMIT в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), сообщение.</span><span class="sxs-lookup"><span data-stu-id="eedec-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="eedec-107">Поставщик хранения сообщений, если тесно связана с поставщиком транспорта, предоставляет сообщение непосредственно к транспорта, который обеспечивает к системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="eedec-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="eedec-108">Если не тесно соединенного, поставщик хранения сообщений информирует диспетчер очереди MAPI, который был изменен в очереди исходящих сообщений и диспетчер очереди MAPI передает сообщения поставщика соответствующий транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="eedec-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="eedec-109">Если разрешить пользователям отменять операцию отправки, вызовите [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="eedec-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="eedec-110">**AbortSubmit** удаляет сообщение из очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="eedec-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="eedec-111">Пользователям можно разрешить для остановки отправки из сведений о событиях пока сообщение назначается базовым системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="eedec-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="eedec-112">Если **SubmitMessage** возвращает MAPI_E_CORRUPT_DATA, предположим, что отправляемых данных теперь потеряны.</span><span class="sxs-lookup"><span data-stu-id="eedec-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="eedec-113">Прежде чем отправить еще раз, повторно записи сообщения путем вызова [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="eedec-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="eedec-114">Сообщение об ошибке для пользователя, если эти вызовы **IMAPIProp** с ошибкой или **SubmitMessage** не удается выполнить еще раз.</span><span class="sxs-lookup"><span data-stu-id="eedec-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="eedec-115">После успешного вызова **SubmitMessage**освободить память, выделенная для списка получателей и освободить сообщение и его вложения.</span><span class="sxs-lookup"><span data-stu-id="eedec-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="eedec-116">После отправки сообщения MAPI не разрешает дополнительные операции с указателями для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="eedec-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="eedec-117">Одно исключение — это вызов **функции IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="eedec-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="eedec-118">Другие вызовы не разрешены, так как многие поставщики хранилища сообщений недействительными идентификаторы записей для сообщений, отправленных.</span><span class="sxs-lookup"><span data-stu-id="eedec-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

