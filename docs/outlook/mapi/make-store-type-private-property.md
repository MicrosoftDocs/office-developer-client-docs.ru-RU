---
title: Сделать личное свойство типа хранилища
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298469"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="89bc6-103">Сделать личное свойство типа хранилища</span><span class="sxs-lookup"><span data-stu-id="89bc6-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="89bc6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89bc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89bc6-105">РасСматривает вторичное хранилище как личное.</span><span class="sxs-lookup"><span data-stu-id="89bc6-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89bc6-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="89bc6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89bc6-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="89bc6-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="89bc6-108">[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="89bc6-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="89bc6-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="89bc6-109">Created by:</span></span>  <br/> |<span data-ttu-id="89bc6-110">Поставщик хранилища</span><span class="sxs-lookup"><span data-stu-id="89bc6-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="89bc6-111">Доступ:</span><span class="sxs-lookup"><span data-stu-id="89bc6-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="89bc6-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="89bc6-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="89bc6-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="89bc6-113">Property type:</span></span>  <br/> |<span data-ttu-id="89bc6-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="89bc6-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="89bc6-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="89bc6-115">Access type:</span></span>  <br/> |<span data-ttu-id="89bc6-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89bc6-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89bc6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="89bc6-117">Remarks</span></span>

<span data-ttu-id="89bc6-118">Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) и вернуть допустимый тег свойства для любого из этих свойств, передаваемого в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="89bc6-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="89bc6-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::](imapiprop-getprops.md)-Props, поставщик хранилища также должен возвращать правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="89bc6-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="89bc6-120">Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств.</span><span class="sxs-lookup"><span data-stu-id="89bc6-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="89bc6-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="89bc6-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="89bc6-122">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="89bc6-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89bc6-123">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="89bc6-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="89bc6-124">ПС_ПУБЛИК_СТРИНГС</span><span class="sxs-lookup"><span data-stu-id="89bc6-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="89bc6-125">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="89bc6-125">ulKind:</span></span>  <br/> |<span data-ttu-id="89bc6-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="89bc6-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="89bc6-127">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="89bc6-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="89bc6-128">L "urn: schemas-microsoft-com: Office: Outlook # сторетипепривате"</span><span class="sxs-lookup"><span data-stu-id="89bc6-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="89bc6-129">Поставщик магазина может использовать это свойство, чтобы приложение Outlook считало его конфиденциальным, если он является дополнительным хранилищем для пользователя.</span><span class="sxs-lookup"><span data-stu-id="89bc6-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="89bc6-130">По умолчанию Outlook рассматривает дополнительное хранилище так же, как и хранилище делегата, а элементы в дополнительном хранилище — частными, только если пользователь помечает их как частные.</span><span class="sxs-lookup"><span data-stu-id="89bc6-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="89bc6-131">Если это свойство имеет **значение true**, элементы, удаленные из дополнительного хранилища, перемещаются в папку " **Удаленные** " в основном хранилище.</span><span class="sxs-lookup"><span data-stu-id="89bc6-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="89bc6-132">Элементы, помеченные как частные, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="89bc6-132">Items marked private are not displayed.</span></span> <span data-ttu-id="89bc6-133">Черновики хранятся в папке "Черновики" в основном хранилище.</span><span class="sxs-lookup"><span data-stu-id="89bc6-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="89bc6-134">Это свойство игнорируется, если версия Outlook более ранняя, чем Microsoft Office Outlook 2003 с пакетом обновления 1 (SP1), или если его значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="89bc6-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

