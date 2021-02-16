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
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434678"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="0c176-103">Обработка отправленного сообщения</span><span class="sxs-lookup"><span data-stu-id="0c176-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="0c176-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c176-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c176-105">Исходящие сообщения после их передачи можно оставить в папке "Исходящие", в папку, предназначенную для удержания отправленных сообщений, или удалить.</span><span class="sxs-lookup"><span data-stu-id="0c176-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="0c176-106">Тип обработки зависит от того, установлены ли свойства хранения сообщений:</span><span class="sxs-lookup"><span data-stu-id="0c176-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="0c176-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0c176-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0c176-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0c176-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="0c176-109">**PR_DELETE_AFTER_SUBMIT** является boolean свойством, заданным как TRUE, если сообщения должны быть удалены после их и в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="0c176-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="0c176-110">**PR_SENTMAIL_ENTRYID** является идентификатором записи папки.</span><span class="sxs-lookup"><span data-stu-id="0c176-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="0c176-111">Если за установлено это свойство, необходимо переместить отправленные сообщения в папку, представленную идентификатором этой записи.</span><span class="sxs-lookup"><span data-stu-id="0c176-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="0c176-112">Сохраненные сообщения обычно имеют удостоверение последнего поставщика личных сообщений или поставщика транспорта для их отправки.</span><span class="sxs-lookup"><span data-stu-id="0c176-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="0c176-113">Либо одно, либо другое, либо ни одно из этих свойств не должно быть установлено, но не оба.</span><span class="sxs-lookup"><span data-stu-id="0c176-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="0c176-114">Однако если вы **PR_SENTMAIL_ENTRYID,** он должен содержать допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="0c176-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="0c176-115">В следующей таблице описано, как эти свойства влияют на работу с отправленными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0c176-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c176-116">Если ни одно из свойств не за установлено:</span><span class="sxs-lookup"><span data-stu-id="0c176-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="0c176-117">Оставьте сообщение в папке, из которой оно было отправлено (как правило, в папке "Из папки").</span><span class="sxs-lookup"><span data-stu-id="0c176-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="0c176-118">Если **PR_SENTMAIL_ENTRYID** установлено:</span><span class="sxs-lookup"><span data-stu-id="0c176-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="0c176-119">Переместит сообщение в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="0c176-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="0c176-120">Если **PR_DELETE_AFTER_SUBMIT** установлено:</span><span class="sxs-lookup"><span data-stu-id="0c176-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="0c176-121">Удалите сообщение.</span><span class="sxs-lookup"><span data-stu-id="0c176-121">Delete the message.</span></span>  <br/> |
   

