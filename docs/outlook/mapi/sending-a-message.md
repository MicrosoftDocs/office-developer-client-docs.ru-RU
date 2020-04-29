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
# <a name="sending-a-message"></a><span data-ttu-id="57b44-103">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="57b44-103">Sending a Message</span></span>

  
  
<span data-ttu-id="57b44-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57b44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57b44-105">Когда вы будете готовы отправить сообщение, вызовите его метод [iMessage:: субмитмессаже](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="57b44-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="57b44-106">**Субмитмессаже** помещает сообщение в очередь исходящих сообщений и устанавливает флаг MSGFLAG_SUBMIT в свойстве **PR_MESSAGE_FLAGS** сообщения ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="57b44-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="57b44-107">Поставщик хранилища сообщений, если он тесно связан с поставщиком транспорта, передает сообщение непосредственно транспорту, который доставляет его в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="57b44-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="57b44-108">Если он не тесно связан, поставщик хранилища сообщений информирует диспетчер очереди сообщений об изменении очереди исходящей почты, а диспетчер очереди MAPI передает сообщение соответствующему поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="57b44-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="57b44-109">Если вы разрешите пользователям отменить операцию отправки, вызовите [IMsgStore:: абортсубмит](imsgstore-abortsubmit.md) , чтобы реализовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="57b44-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="57b44-110">**Абортсубмит** удаляет сообщение из исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="57b44-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="57b44-111">Пользователям может быть разрешено остановить отправку, пока сообщение не будет получено в базовую систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="57b44-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="57b44-112">Если **субмитмессаже** возвращает MAPI_E_CORRUPT_DATA, предполагается, что отправляемые данные будут утрачены.</span><span class="sxs-lookup"><span data-stu-id="57b44-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="57b44-113">Прежде чем пытаться отправить сообщение еще раз, перепишите его, вызвав [IMAPIProp:: SetProps](imapiprop-setprops.md) и [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="57b44-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="57b44-114">Показывать пользователю сообщение об ошибке, если эти вызовы **IMAPIProp** не выполнены или если **субмитмессаже** не удается выполнить второй раз.</span><span class="sxs-lookup"><span data-stu-id="57b44-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="57b44-115">После успешного вызова **субмитмессаже**освободите память, выделенную для списка получателей, и освободите сообщение и его вложения.</span><span class="sxs-lookup"><span data-stu-id="57b44-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="57b44-116">После отправки сообщения MAPI не разрешает дальнейшие операции с указателями для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="57b44-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="57b44-117">Единственным исключением является вызов **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="57b44-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="57b44-118">Другие вызовы не разрешены, так как многие поставщики хранилищ сообщений делают недействительными идентификаторы записей для отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="57b44-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

