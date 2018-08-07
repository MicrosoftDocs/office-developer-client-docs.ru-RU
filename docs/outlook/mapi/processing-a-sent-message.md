---
title: Обработка отправленного сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812054"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="66d7b-103">Обработка отправленного сообщения</span><span class="sxs-lookup"><span data-stu-id="66d7b-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="66d7b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66d7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66d7b-105">Исходящим сообщениям, после их передачи может оставаться в папке Исходящие папки, перемещаются в папку, предназначенный для хранения отправленных сообщений или удалении.</span><span class="sxs-lookup"><span data-stu-id="66d7b-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="66d7b-106">Тип обработки зависит от того, является ли вы задали сообщение хранилища свойств:</span><span class="sxs-lookup"><span data-stu-id="66d7b-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="66d7b-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66d7b-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="66d7b-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66d7b-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="66d7b-109">**PR_DELETE_AFTER_SUBMIT** — это логическое свойство, присвоено значение TRUE, если после их отправки подлежащий удалению сообщения и FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="66d7b-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="66d7b-110">**PR_SENTMAIL_ENTRYID** — это идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="66d7b-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="66d7b-111">Если задано это свойство, следует переместить отправленных сообщений в папку, представленного в этом идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="66d7b-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="66d7b-112">Обычно сохраненные сообщения со свойством IDENTITY, последний хранилища сообщений или транспорта поставщика для их отправки.</span><span class="sxs-lookup"><span data-stu-id="66d7b-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="66d7b-113">Одно или другое или ни один из этих свойств должно быть набор, но не оба.</span><span class="sxs-lookup"><span data-stu-id="66d7b-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="66d7b-114">Тем не менее если значение **PR_SENTMAIL_ENTRYID**, он должен содержать идентификатор допустимый записи.</span><span class="sxs-lookup"><span data-stu-id="66d7b-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="66d7b-115">В следующей таблице описываются, как эти свойства влияют на что можно сделать с помощью отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="66d7b-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66d7b-116">Если ни один из свойство имеет значение:</span><span class="sxs-lookup"><span data-stu-id="66d7b-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="66d7b-117">Оставьте сообщение в папку, из которого был отправлен (обычно исходящие).</span><span class="sxs-lookup"><span data-stu-id="66d7b-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="66d7b-118">Если значение **PR_SENTMAIL_ENTRYID** :</span><span class="sxs-lookup"><span data-stu-id="66d7b-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="66d7b-119">Перемещение сообщения в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="66d7b-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="66d7b-120">Если значение **PR_DELETE_AFTER_SUBMIT** :</span><span class="sxs-lookup"><span data-stu-id="66d7b-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="66d7b-121">Удалите сообщение.</span><span class="sxs-lookup"><span data-stu-id="66d7b-121">Delete the message.</span></span>  <br/> |
   

