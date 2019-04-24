---
title: Поддержка доступа к объектам и их сравнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349611"
---
# <a name="supporting-object-access-and-comparison"></a><span data-ttu-id="2e11a-103">Поддержка доступа к объектам и их сравнения</span><span class="sxs-lookup"><span data-stu-id="2e11a-103">Supporting Object Access and Comparison</span></span>

  
  
<span data-ttu-id="2e11a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e11a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e11a-105">Поставщики услуг могут использовать методы [имаписуппорт:: OpenEntry](imapisupport-openentry.md) и [Имаписуппорт:: метод compareentryids](imapisupport-compareentryids.md) для открытия и сравнения объектов, принадлежащих их поставщику или другим поставщикам:</span><span class="sxs-lookup"><span data-stu-id="2e11a-105">Service providers can use the [IMAPISupport::OpenEntry](imapisupport-openentry.md) and [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) methods to open and compare objects that belong to their provider or to other providers:</span></span> 
  
<span data-ttu-id="2e11a-106">Как и [IMAPISession:: OpenEntry](imapisession-openentry.md) для клиентов, поставщики могут использовать метод **OpenEntry** объекта support для доступа к любому объекту, если он известен идентификатору записи объекта.</span><span class="sxs-lookup"><span data-stu-id="2e11a-106">Like [IMAPISession::OpenEntry](imapisession-openentry.md) for clients, providers can use their support object's **OpenEntry** method to access any object as long they know the object's entry identifier.</span></span> <span data-ttu-id="2e11a-107">В отличие от метода Session, метод поддержки требует указать допустимый идентификатор записи в параметре _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="2e11a-107">Unlike the session method, the support method requires that you specify a valid entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="2e11a-108">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2e11a-108">It cannot be NULL.</span></span> 
  
<span data-ttu-id="2e11a-109">Чтобы продемонстрировать, как поставщик транспорта может использовать **имаписуппорт:: OpenEntry**, рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="2e11a-109">To illustrate how a transport provider might use **IMAPISupport::OpenEntry**, consider the following scenario.</span></span> <span data-ttu-id="2e11a-110">Поставщик транспорта получил сообщение, отформатированное в формате RTF, и не знает, может ли целевой получатель обрабатывать этот формат.</span><span class="sxs-lookup"><span data-stu-id="2e11a-110">The transport provider has received a message formatted in Rich Text Format and does not know whether the target recipient can handle this format.</span></span> <span data-ttu-id="2e11a-111">Перед доставкой сообщения поставщик транспорта должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2e11a-111">Before delivering the message, the transport provider needs to do the following:</span></span>
  
1. <span data-ttu-id="2e11a-112">ВыЗовите метод [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) , чтобы получить доступ к таблице получателей и идентификатору записи получателя, его свойству **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2e11a-112">Call the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method to access the recipient table and the recipient's entry identifier, its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="2e11a-113">Передайте идентификатор записи в **имаписуппорт:: OpenEntry** , чтобы открыть получателя, обычно это либо пользователь обмена сообщениями, либо список рассылки.</span><span class="sxs-lookup"><span data-stu-id="2e11a-113">Pass the entry identifier to **IMAPISupport::OpenEntry** to open the recipient, typically either a messaging user or distribution list.</span></span> <span data-ttu-id="2e11a-114">Для параметра _лпинтерфаце_ должно быть ЗАДАНО значение null, так как поставщик не может заранее знать тип объекта получателя.</span><span class="sxs-lookup"><span data-stu-id="2e11a-114">The  _lpInterface_ parameter should be set to NULL because the provider cannot know ahead of time the object type of the recipient.</span></span> <span data-ttu-id="2e11a-115">Метод **OpenEntry** объекта support вызывает [IMAPISession:: OpenEntry](imapisession-openentry.md) для определения поставщика адресных книг, ответственного за получателя.</span><span class="sxs-lookup"><span data-stu-id="2e11a-115">The support object's **OpenEntry** method calls [IMAPISession::OpenEntry](imapisession-openentry.md) to determine the address book provider responsible for the recipient.</span></span> <span data-ttu-id="2e11a-116">Затем объект Session вызывает соответствующий метод поставщика адресных книг **OpenEntry** , чтобы открыть получателя и вернуть указатель интерфейса поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="2e11a-116">The session object then calls the appropriate address book provider's **OpenEntry** method to open the recipient and return an interface pointer to the transport provider.</span></span> 
    
3. <span data-ttu-id="2e11a-117">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS получателя, чтобы получить свойство **пр_сенд_рич_инфо** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2e11a-117">Call the recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="2e11a-118">Если для **пр_сенд_рич_инфо** ЗАДАНО значение true, получатель может обрабатывать форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="2e11a-118">If **PR_SEND_RICH_INFO** is set to TRUE, the recipient can handle formatted text.</span></span> 
    
<span data-ttu-id="2e11a-119">Если вы открыли несколько объектов от других поставщиков, вам может потребоваться выяснить, ссылаются ли два идентификатора записи на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="2e11a-119">If you have opened several objects from other providers, you may need to find out whether two entry identifiers refer to the same object.</span></span> <span data-ttu-id="2e11a-120">Например, у вас может быть краткосрочный идентификатор записи и долгосрочный идентификатор записи, и эти идентификаторы могут не определять один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="2e11a-120">For example, you may have a short-term entry identifier and a long-term entry identifier and these identifiers may or may not identify the same object.</span></span> <span data-ttu-id="2e11a-121">Во избежание избыточной обработки вызовите метод [имаписуппорт:: метод compareentryids](imapisupport-compareentryids.md) для сравнения этих идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="2e11a-121">To avoid redundant processing, call the [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) method to compare these entry identifiers.</span></span> <span data-ttu-id="2e11a-122">Этот метод необходимо использовать для сравнения идентификатора записи, так как идентификаторы записей не могут сравниваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="2e11a-122">You must use this method for entry identifier comparison because entry identifiers cannot be compared directly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e11a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2e11a-123">See also</span></span>



[<span data-ttu-id="2e11a-124">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="2e11a-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

