---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810037"
---
# <a name="nofolderscan"></a><span data-ttu-id="24af7-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="24af7-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="24af7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24af7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24af7-105">Указывает, будет ли Microsoft Office Outlook необходимо сканировать папки Контакты для хранилища.</span><span class="sxs-lookup"><span data-stu-id="24af7-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="24af7-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="24af7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24af7-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="24af7-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="24af7-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="24af7-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="24af7-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="24af7-109">Created by:</span></span>  <br/> |<span data-ttu-id="24af7-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="24af7-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="24af7-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="24af7-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="24af7-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="24af7-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="24af7-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="24af7-113">Property type:</span></span>  <br/> |<span data-ttu-id="24af7-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24af7-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24af7-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="24af7-115">Access type:</span></span>  <br/> |<span data-ttu-id="24af7-116">Только чтение или чтение и запись в зависимости от поставщика хранилища</span><span class="sxs-lookup"><span data-stu-id="24af7-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24af7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="24af7-117">Remarks</span></span>

<span data-ttu-id="24af7-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="24af7-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="24af7-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="24af7-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="24af7-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="24af7-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="24af7-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="24af7-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="24af7-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="24af7-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24af7-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="24af7-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="24af7-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="24af7-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="24af7-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="24af7-125">ulKind:</span></span>  <br/> |<span data-ttu-id="24af7-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="24af7-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="24af7-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="24af7-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="24af7-128">L «NoFolderScan»</span><span class="sxs-lookup"><span data-stu-id="24af7-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="24af7-129">Это свойство предоставляет способ для хранения поставщиков для указания в Outlook не сканировать папки Контакты в хранилище, чтобы предотвратить снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="24af7-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="24af7-130">Она используется в операции слияния почты, во время которых Outlook проверяет наличие и значение этого свойства перед началом сканирования.</span><span class="sxs-lookup"><span data-stu-id="24af7-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="24af7-131">По умолчанию это свойство не предоставляется для хранилища, это значит, что Outlook поддерживает сканирование папки Контакты в хранилище.</span><span class="sxs-lookup"><span data-stu-id="24af7-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="24af7-132">Если свойство предоставляется, ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="24af7-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="24af7-133">Нуль (0): Outlook можно выполнить проверку.</span><span class="sxs-lookup"><span data-stu-id="24af7-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="24af7-134">Ненулевое значение: Outlook не следует сканировать списка контактов пользователя в хранилище.</span><span class="sxs-lookup"><span data-stu-id="24af7-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

