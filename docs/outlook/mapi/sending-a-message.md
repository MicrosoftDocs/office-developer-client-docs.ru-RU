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
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423624"
---
# <a name="sending-a-message"></a><span data-ttu-id="f7cf2-103">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="f7cf2-103">Sending a Message</span></span>

  
  
<span data-ttu-id="f7cf2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7cf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7cf2-105">Когда вы готовы отправить сообщение, позвоните по методу [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="f7cf2-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="f7cf2-106">**SubmitMessage** помещает сообщение в исходячую очередь и задает флаг MSGFLAG_SUBMIT в  свойстве [PR_MESSAGE_FLAGS (PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f7cf2-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f7cf2-107">Поставщик хранения сообщений, если он тесно связан с поставщиком транспорта, передает сообщение непосредственно транспорту, который доставляет его в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="f7cf2-108">Если это не тесно, поставщик магазина сообщений информирует spooler MAPI о том, что исходяя очередь изменилась, а пуллер MAPI передает сообщение соответствующему поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="f7cf2-109">Если вы позволите пользователям отменить операцию отправки, позвоните [в IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="f7cf2-110">**AbortSubmit** удаляет сообщение из исходявой очереди.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="f7cf2-111">Пользователям может быть разрешено остановить отправку до тех пор, пока сообщение не будет передано в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="f7cf2-112">Если **SubmitMessage** возвращает MAPI_E_CORRUPT_DATA, предположим, что отправленные данные потеряны.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="f7cf2-113">Перед повторной отправкой перепишите сообщение, позвонив [в IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="f7cf2-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="f7cf2-114">Отображение ошибки для пользователя, если эти **вызовы IMAPIProp** сбой или **если SubmitMessage** не во второй раз.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="f7cf2-115">После успешного вызова **в SubmitMessage** освободите любую память, выделенную для списка получателей, и освободите сообщение и его вложения.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="f7cf2-116">После отправления сообщения MAPI не разрешает дальнейшие операции в указателях для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="f7cf2-117">Исключением является вызов **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="f7cf2-118">Другие вызовы не допускаются, так как многие поставщики магазинов сообщений недействительны идентификаторы записей для отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7cf2-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

