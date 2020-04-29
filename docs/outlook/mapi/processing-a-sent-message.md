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
# <a name="processing-a-sent-message"></a><span data-ttu-id="cf592-103">Обработка отправленного сообщения</span><span class="sxs-lookup"><span data-stu-id="cf592-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="cf592-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf592-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf592-105">Исходящие сообщения, после их отправки, можно оставить в папке "Исходящие", переместить в папку, предназначенную для хранения отправленных сообщений, или удалить.</span><span class="sxs-lookup"><span data-stu-id="cf592-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="cf592-106">Тип обработки зависит от того, настроены ли свойства хранилища сообщений:</span><span class="sxs-lookup"><span data-stu-id="cf592-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="cf592-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cf592-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="cf592-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cf592-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="cf592-109">**PR_DELETE_AFTER_SUBMIT** является логическим свойством, имеет значение true, если после отправки сообщения необходимо удалить, а в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="cf592-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="cf592-110">**PR_SENTMAIL_ENTRYID** — это идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="cf592-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="cf592-111">Если это свойство задано, вы должны переместить отправленные сообщения в папку, представленную этим идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="cf592-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="cf592-112">Сохраненные сообщения обычно имеют идентификатор последнего хранилища сообщений или поставщика транспорта для их отправки.</span><span class="sxs-lookup"><span data-stu-id="cf592-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="cf592-113">Не должно быть задано ни одно из этих свойств либо ни то, ни другое.</span><span class="sxs-lookup"><span data-stu-id="cf592-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="cf592-114">Тем не менее, если вы настроили **PR_SENTMAIL_ENTRYID**, он должен содержать допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="cf592-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="cf592-115">В следующей таблице показано, как эти свойства влияют на действия, выполняемые с отправленными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cf592-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf592-116">Если не задано ни одно свойство:</span><span class="sxs-lookup"><span data-stu-id="cf592-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="cf592-117">Оставьте сообщение в папке, из которой оно было отправлено (обычно это папка "исходящая").</span><span class="sxs-lookup"><span data-stu-id="cf592-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="cf592-118">Если параметр **PR_SENTMAIL_ENTRYID** задан:</span><span class="sxs-lookup"><span data-stu-id="cf592-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="cf592-119">Переместить сообщение в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="cf592-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="cf592-120">Если параметр **PR_DELETE_AFTER_SUBMIT** задан:</span><span class="sxs-lookup"><span data-stu-id="cf592-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="cf592-121">Удаление сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf592-121">Delete the message.</span></span>  <br/> |
   

