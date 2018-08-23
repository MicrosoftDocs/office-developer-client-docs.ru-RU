---
title: Свойство, делающее тип хранилища частным
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
ms.openlocfilehash: 2d927b00391725d8804e41b66b1ec8c384f98e7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568835"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="aa871-103">Свойство, делающее тип хранилища частным</span><span class="sxs-lookup"><span data-stu-id="aa871-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="aa871-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa871-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa871-105">Рассматривается как закрытый дополнительного хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa871-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aa871-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="aa871-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa871-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="aa871-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="aa871-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="aa871-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="aa871-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="aa871-109">Created by:</span></span>  <br/> |<span data-ttu-id="aa871-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="aa871-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="aa871-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="aa871-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="aa871-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="aa871-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="aa871-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="aa871-113">Property type:</span></span>  <br/> |<span data-ttu-id="aa871-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="aa871-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="aa871-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="aa871-115">Access type:</span></span>  <br/> |<span data-ttu-id="aa871-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aa871-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa871-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="aa871-117">Remarks</span></span>

<span data-ttu-id="aa871-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="aa871-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="aa871-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="aa871-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="aa871-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="aa871-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="aa871-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="aa871-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="aa871-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="aa871-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa871-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="aa871-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="aa871-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="aa871-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="aa871-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="aa871-125">ulKind:</span></span>  <br/> |<span data-ttu-id="aa871-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="aa871-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="aa871-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="aa871-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="aa871-128">L "urn: schemas-microsoft-com:office:outlook #storetypeprivate»</span><span class="sxs-lookup"><span data-stu-id="aa871-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="aa871-129">Это свойство можно использовать поставщика хранилища будет считать его закрытого при дополнительного хранилища для пользователя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="aa871-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="aa871-130">По умолчанию Outlook считает дополнительного хранилища так же, как делегат хранилища и элементов в хранилище дополнительного частной, только если им специально частных.</span><span class="sxs-lookup"><span data-stu-id="aa871-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="aa871-131">Когда это свойство имеет **значение true**, элементы, удаленные из дополнительного хранилища перемещаются в папку " **Удаленные** " в основного хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa871-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="aa871-132">Личным не отображаются.</span><span class="sxs-lookup"><span data-stu-id="aa871-132">Items marked private are not displayed.</span></span> <span data-ttu-id="aa871-133">«Черновики», хранятся в папке «Черновики» в основного хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa871-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="aa871-134">Это свойство игнорируется, если используется Outlook версии более ранней, чем пакет обновления 1 для Microsoft Office Outlook 2003 или имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="aa871-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

