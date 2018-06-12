---
title: Поддержка доступа к объектам и сравнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 2152cfbb91f2e343ebcee3f5b717a29805df1d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812446"
---
# <a name="supporting-object-access-and-comparison"></a><span data-ttu-id="9478d-103">Поддержка доступа к объектам и сравнения</span><span class="sxs-lookup"><span data-stu-id="9478d-103">Supporting Object Access and Comparison</span></span>

  
  
<span data-ttu-id="9478d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9478d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9478d-105">Поставщики услуг могут использовать методы [IMAPISupport::OpenEntry](imapisupport-openentry.md) и [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) для открытия и сравнения объектов, которые принадлежат своим поставщиком или других поставщиков:</span><span class="sxs-lookup"><span data-stu-id="9478d-105">Service providers can use the [IMAPISupport::OpenEntry](imapisupport-openentry.md) and [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) methods to open and compare objects that belong to their provider or to other providers:</span></span> 
  
<span data-ttu-id="9478d-106">Как [IMAPISession::OpenEntry](imapisession-openentry.md) для клиентов поставщиков можно использовать метод **OpenEntry** их поддержка объекта для доступа к любой объект, как долго знают идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="9478d-106">Like [IMAPISession::OpenEntry](imapisession-openentry.md) for clients, providers can use their support object's **OpenEntry** method to access any object as long they know the object's entry identifier.</span></span> <span data-ttu-id="9478d-107">В отличие от метода сеанса метод поддержки необходимо указать идентификатор допустимый записи с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9478d-107">Unlike the session method, the support method requires that you specify a valid entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="9478d-108">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="9478d-108">It cannot be NULL.</span></span> 
  
<span data-ttu-id="9478d-109">Чтобы показать, как использовать **IMAPISupport::OpenEntry**поставщика транспорта, рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="9478d-109">To illustrate how a transport provider might use **IMAPISupport::OpenEntry**, consider the following scenario.</span></span> <span data-ttu-id="9478d-110">Поставщика транспорта получил сообщение, отформатированные в формате RTF и не имеет ли получатель целевой можно обрабатывать в этом формате.</span><span class="sxs-lookup"><span data-stu-id="9478d-110">The transport provider has received a message formatted in Rich Text Format and does not know whether the target recipient can handle this format.</span></span> <span data-ttu-id="9478d-111">Перед доставкой сообщения, поставщика транспорта должно выполнять следующее:</span><span class="sxs-lookup"><span data-stu-id="9478d-111">Before delivering the message, the transport provider needs to do the following:</span></span>
  
1. <span data-ttu-id="9478d-112">Вызовите метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) сообщений для доступа к таблице получателей и идентификатор записи получателя, его свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9478d-112">Call the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method to access the recipient table and the recipient's entry identifier, its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="9478d-113">Передайте идентификатор записи **IMAPISupport::OpenEntry** для открытия получателя, обычно либо обмена сообщениями пользователя или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="9478d-113">Pass the entry identifier to **IMAPISupport::OpenEntry** to open the recipient, typically either a messaging user or distribution list.</span></span> <span data-ttu-id="9478d-114">Параметр _lpInterface_ необходимо задать значение NULL, так как поставщик не может знать заранее тип объекта получателя.</span><span class="sxs-lookup"><span data-stu-id="9478d-114">The  _lpInterface_ parameter should be set to NULL because the provider cannot know ahead of time the object type of the recipient.</span></span> <span data-ttu-id="9478d-115">Метод **OpenEntry** объекта поддержки вызывает [IMAPISession::OpenEntry](imapisession-openentry.md) для определения поставщик адресной книги, ответственный за получателя.</span><span class="sxs-lookup"><span data-stu-id="9478d-115">The support object's **OpenEntry** method calls [IMAPISession::OpenEntry](imapisession-openentry.md) to determine the address book provider responsible for the recipient.</span></span> <span data-ttu-id="9478d-116">Объект сеанса затем вызывает метод **OpenEntry** поставщик соответствующие адресной книги для открытия получателя и возвращает указатель интерфейса поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="9478d-116">The session object then calls the appropriate address book provider's **OpenEntry** method to open the recipient and return an interface pointer to the transport provider.</span></span> 
    
3. <span data-ttu-id="9478d-117">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) получателя для получения его свойство **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9478d-117">Call the recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="9478d-118">Если **PR_SEND_RICH_INFO** имеет значение TRUE, получатель может обрабатывать форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="9478d-118">If **PR_SEND_RICH_INFO** is set to TRUE, the recipient can handle formatted text.</span></span> 
    
<span data-ttu-id="9478d-119">При открытии нескольких объектов из других поставщиков может потребоваться узнать ли двух идентификаторов запись ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="9478d-119">If you have opened several objects from other providers, you may need to find out whether two entry identifiers refer to the same object.</span></span> <span data-ttu-id="9478d-120">Например в некоторых случаях краткосрочных идентификатор записи и долгосрочного идентификатор записи этих идентификаторов может и не может определить тот же объект.</span><span class="sxs-lookup"><span data-stu-id="9478d-120">For example, you may have a short-term entry identifier and a long-term entry identifier and these identifiers may or may not identify the same object.</span></span> <span data-ttu-id="9478d-121">Чтобы избежать избыточных обработки, вызовите метод [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) для сравнения этих идентификаторов запись.</span><span class="sxs-lookup"><span data-stu-id="9478d-121">To avoid redundant processing, call the [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) method to compare these entry identifiers.</span></span> <span data-ttu-id="9478d-122">Этот метод необходимо использовать для сравнения идентификатор записи, так как идентификаторы записей нельзя сравнивать непосредственно.</span><span class="sxs-lookup"><span data-stu-id="9478d-122">You must use this method for entry identifier comparison because entry identifiers cannot be compared directly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9478d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9478d-123">See also</span></span>



[<span data-ttu-id="9478d-124">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="9478d-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

