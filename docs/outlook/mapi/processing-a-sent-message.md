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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351067"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="42783-103">Обработка отправленного сообщения</span><span class="sxs-lookup"><span data-stu-id="42783-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="42783-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42783-105">ИсХодящие сообщения, после их отправки, можно оставить в папке "исХодящие", переместить в папку, предназначенную для хранения отправленных сообщений, или удалить.</span><span class="sxs-lookup"><span data-stu-id="42783-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="42783-106">Тип обработки зависит от того, настроены ли свойства хранилища сообщений:</span><span class="sxs-lookup"><span data-stu-id="42783-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="42783-107">**Пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="42783-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="42783-108">**Пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="42783-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="42783-109">**Пр_делете_афтер_субмит** является логическим свойством, имеет значение true, если после отправки сообщения необходимо удалить, а в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="42783-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="42783-110">**Пр_сентмаил_ентрид** — идентификатор элемента папки.</span><span class="sxs-lookup"><span data-stu-id="42783-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="42783-111">Если это свойство задано, вы должны переместить отправленные сообщения в папку, представленную этим идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="42783-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="42783-112">Сохраненные сообщения обычно имеют идентификатор последнего хранилища сообщений или поставщика транспорта для их отправки.</span><span class="sxs-lookup"><span data-stu-id="42783-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="42783-113">Не должно быть задано ни одно из этих свойств либо ни то, ни другое.</span><span class="sxs-lookup"><span data-stu-id="42783-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="42783-114">Тем не менее, если вы настроили **пр_сентмаил_ентрид**, он должен содержать допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="42783-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="42783-115">В следующей таблице показано, как эти свойства влияют на действия, выполняемые с отправленными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="42783-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42783-116">Если не задано ни одно свойство:</span><span class="sxs-lookup"><span data-stu-id="42783-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="42783-117">Оставьте сообщение в папке, из которой оно было отправлено (обычно это папка "исХодящая").</span><span class="sxs-lookup"><span data-stu-id="42783-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="42783-118">Если задано значение **пр_сентмаил_ентрид** :</span><span class="sxs-lookup"><span data-stu-id="42783-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="42783-119">Переместить сообщение в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="42783-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="42783-120">Если задано значение **пр_делете_афтер_субмит** :</span><span class="sxs-lookup"><span data-stu-id="42783-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="42783-121">Удаление сообщения.</span><span class="sxs-lookup"><span data-stu-id="42783-121">Delete the message.</span></span>  <br/> |
   

