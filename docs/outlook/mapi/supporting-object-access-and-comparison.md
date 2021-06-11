---
title: Поддержка доступа и сравнения объектов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429035"
---
# <a name="supporting-object-access-and-comparison"></a><span data-ttu-id="f42b6-103">Поддержка доступа и сравнения объектов</span><span class="sxs-lookup"><span data-stu-id="f42b6-103">Supporting Object Access and Comparison</span></span>

  
  
<span data-ttu-id="f42b6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f42b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f42b6-105">Поставщики услуг могут использовать методы [IMAPISupport::OpenEntry](imapisupport-openentry.md) и [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) для открытия и сравнения объектов, принадлежащих их поставщику или другим поставщикам:</span><span class="sxs-lookup"><span data-stu-id="f42b6-105">Service providers can use the [IMAPISupport::OpenEntry](imapisupport-openentry.md) and [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) methods to open and compare objects that belong to their provider or to other providers:</span></span> 
  
<span data-ttu-id="f42b6-106">Как [и IMAPISession::OpenEntry](imapisession-openentry.md) для клиентов, поставщики могут использовать метод **OpenEntry** объекта поддержки для доступа к любому объекту до тех пор, пока они знают идентификатор входа объекта.</span><span class="sxs-lookup"><span data-stu-id="f42b6-106">Like [IMAPISession::OpenEntry](imapisession-openentry.md) for clients, providers can use their support object's **OpenEntry** method to access any object as long they know the object's entry identifier.</span></span> <span data-ttu-id="f42b6-107">В отличие от метода сеанса, метод поддержки требует указать допустимый идентификатор входа в _параметре lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="f42b6-107">Unlike the session method, the support method requires that you specify a valid entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="f42b6-108">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f42b6-108">It cannot be NULL.</span></span> 
  
<span data-ttu-id="f42b6-109">Чтобы проиллюстрировать, как поставщик транспорта может использовать **IMAPISupport::OpenEntry,** рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="f42b6-109">To illustrate how a transport provider might use **IMAPISupport::OpenEntry**, consider the following scenario.</span></span> <span data-ttu-id="f42b6-110">Поставщик транспорта получил сообщение в формате Rich Text Format и не знает, может ли целевой получатель обрабатывать этот формат.</span><span class="sxs-lookup"><span data-stu-id="f42b6-110">The transport provider has received a message formatted in Rich Text Format and does not know whether the target recipient can handle this format.</span></span> <span data-ttu-id="f42b6-111">Перед доставкой сообщения поставщику транспорта необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="f42b6-111">Before delivering the message, the transport provider needs to do the following:</span></span>
  
1. <span data-ttu-id="f42b6-112">Вызывай метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) для доступа к таблице получателей и идентификатору входа получателя, его свойству PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="f42b6-112">Call the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method to access the recipient table and the recipient's entry identifier, its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="f42b6-113">Передай идентификатор входа **в IMAPISupport::OpenEntry,** чтобы открыть получателя, как правило, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="f42b6-113">Pass the entry identifier to **IMAPISupport::OpenEntry** to open the recipient, typically either a messaging user or distribution list.</span></span> <span data-ttu-id="f42b6-114">Параметр  _lpInterface_ должен быть задан nULL, так как поставщик не может заранее узнать тип объекта получателя.</span><span class="sxs-lookup"><span data-stu-id="f42b6-114">The  _lpInterface_ parameter should be set to NULL because the provider cannot know ahead of time the object type of the recipient.</span></span> <span data-ttu-id="f42b6-115">Метод **OpenEntry** объекта поддержки вызывает [IMAPISession::OpenEntry](imapisession-openentry.md) для определения поставщика адресной книги, ответственного за получателя.</span><span class="sxs-lookup"><span data-stu-id="f42b6-115">The support object's **OpenEntry** method calls [IMAPISession::OpenEntry](imapisession-openentry.md) to determine the address book provider responsible for the recipient.</span></span> <span data-ttu-id="f42b6-116">Затем объект сеанса вызывает метод **OpenEntry** соответствующего поставщика адресной книги, чтобы открыть получателя и вернуть указатель интерфейса поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="f42b6-116">The session object then calls the appropriate address book provider's **OpenEntry** method to open the recipient and return an interface pointer to the transport provider.</span></span> 
    
3. <span data-ttu-id="f42b6-117">Позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) **получателя,** чтобы получить PR_SEND_RICH_INFO [(PidTagSendRichInfo).](pidtagsendrichinfo-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f42b6-117">Call the recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="f42b6-118">Если **PR_SEND_RICH_INFO** установлено true, получатель может обрабатывать отформатированный текст.</span><span class="sxs-lookup"><span data-stu-id="f42b6-118">If **PR_SEND_RICH_INFO** is set to TRUE, the recipient can handle formatted text.</span></span> 
    
<span data-ttu-id="f42b6-119">Если вы открыли несколько объектов от других поставщиков, может потребоваться выяснить, относятся ли два идентификатора записи к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="f42b6-119">If you have opened several objects from other providers, you may need to find out whether two entry identifiers refer to the same object.</span></span> <span data-ttu-id="f42b6-120">Например, у вас может быть краткосрочный идентификатор записи и долгосрочный идентификатор входа, и эти идентификаторы могут идентифицировать один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="f42b6-120">For example, you may have a short-term entry identifier and a long-term entry identifier and these identifiers may or may not identify the same object.</span></span> <span data-ttu-id="f42b6-121">Чтобы избежать избыточной обработки, позвоните в [метод IMAPISupport::CompareEntryIDs,](imapisupport-compareentryids.md) чтобы сравнить эти идентификаторы записи.</span><span class="sxs-lookup"><span data-stu-id="f42b6-121">To avoid redundant processing, call the [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) method to compare these entry identifiers.</span></span> <span data-ttu-id="f42b6-122">Этот метод необходимо использовать для сравнения идентификаторов входа, так как идентификаторы записей нельзя сравнивать напрямую.</span><span class="sxs-lookup"><span data-stu-id="f42b6-122">You must use this method for entry identifier comparison because entry identifiers cannot be compared directly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f42b6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f42b6-123">See also</span></span>



[<span data-ttu-id="f42b6-124">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="f42b6-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

