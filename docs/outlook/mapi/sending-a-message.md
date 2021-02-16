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
# <a name="sending-a-message"></a><span data-ttu-id="a5f01-103">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="a5f01-103">Sending a Message</span></span>

  
  
<span data-ttu-id="a5f01-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f01-105">Когда вы будете готовы отправить сообщение, вызовите его метод [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="a5f01-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a5f01-106">**SubmitMessage** помещает сообщение в исходяжую очередь и устанавливает флаг MSGFLAG_SUBMIT в свойстве PR_MESSAGE_FLAGS **сообщения** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a5f01-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a5f01-107">Поставщик хранения сообщений, если он тесно связан с поставщиком транспорта, передает сообщение непосредственно в транспорт, который доставляет его в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a5f01-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="a5f01-108">Если он не имеет тесной связи, поставщик хранилище сообщений сообщает пулу MAPI об изменениях очереди исходяющих сообщений и передаче сообщения соответствующему поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="a5f01-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="a5f01-109">Если вы разрешаете пользователям отменять операцию отправки, вызовите [IMsgStore::AbortSubmit,](imsgstore-abortsubmit.md) чтобы реализовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a5f01-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="a5f01-110">**AbortSubmit** удаляет сообщение из исходявой очереди.</span><span class="sxs-lookup"><span data-stu-id="a5f01-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="a5f01-111">Пользователям может быть разрешено останавливать отправку, пока сообщение не будет передано в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a5f01-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="a5f01-112">Если **SubmitMessage** возвращает MAPI_E_CORRUPT_DATA, предположим, что отправляемые данные теперь потеряны.</span><span class="sxs-lookup"><span data-stu-id="a5f01-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="a5f01-113">Перед повторной отправкой перепишите сообщение, вызывая [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="a5f01-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="a5f01-114">Отображение ошибки для пользователя, если эти **вызовы IMAPIProp** не удается или **если SubmitMessage** не удается во второй раз.</span><span class="sxs-lookup"><span data-stu-id="a5f01-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="a5f01-115">После успешного вызова **SubmitMessage** освободите память, выделенную для списка получателей, и освободите сообщение и его вложения.</span><span class="sxs-lookup"><span data-stu-id="a5f01-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="a5f01-116">После того как сообщение отправлено, MAPI не разрешает дальнейшие операции с указателями для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="a5f01-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="a5f01-117">Одно исключение — вызов **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="a5f01-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="a5f01-118">Другие вызовы не разрешены, так как многие поставщики store сообщений не допускают идентификаторы записей для отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a5f01-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

