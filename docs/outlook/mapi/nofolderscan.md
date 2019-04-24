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
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326266"
---
# <a name="nofolderscan"></a><span data-ttu-id="7bbaa-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="7bbaa-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="7bbaa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bbaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bbaa-105">Указывает, должно ли приложение Microsoft Office Outlook сканировать папки контактов в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7bbaa-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7bbaa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bbaa-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="7bbaa-108">[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="7bbaa-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-109">Created by:</span></span>  <br/> |<span data-ttu-id="7bbaa-110">Поставщик хранилища</span><span class="sxs-lookup"><span data-stu-id="7bbaa-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="7bbaa-111">Доступ:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="7bbaa-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="7bbaa-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="7bbaa-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-113">Property type:</span></span>  <br/> |<span data-ttu-id="7bbaa-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7bbaa-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7bbaa-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-115">Access type:</span></span>  <br/> |<span data-ttu-id="7bbaa-116">Только чтение или чтение и запись в зависимости от поставщика услуг хранения</span><span class="sxs-lookup"><span data-stu-id="7bbaa-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bbaa-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bbaa-117">Remarks</span></span>

<span data-ttu-id="7bbaa-118">Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMAPIProp: IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданного в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbaa-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="7bbaa-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::](imapiprop-getprops.md)-Props, поставщик хранилища также должен возвращать правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="7bbaa-120">Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="7bbaa-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="7bbaa-122">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bbaa-123">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="7bbaa-124">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="7bbaa-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7bbaa-125">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-125">ulKind:</span></span>  <br/> |<span data-ttu-id="7bbaa-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="7bbaa-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="7bbaa-127">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="7bbaa-128">L "Нофолдерскан"</span><span class="sxs-lookup"><span data-stu-id="7bbaa-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="7bbaa-129">Это свойство позволяет поставщикам услуг хранения указывать, чтобы Outlook не проводил сканирование папок контактов в хранилище во избежание снижения производительности.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="7bbaa-130">Он используется в операциях слияния почты, в которых Outlook проверяет наличие и значение этого свойства перед началом сканирования.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="7bbaa-131">По умолчанию это свойство не отображается в хранилище, что означает, что Outlook может сканировать папку "Контакты" в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="7bbaa-132">Если свойство предоставлено, могут быть доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="7bbaa-133">Ноль (0): Outlook может выполнить сканирование.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="7bbaa-134">Ненулевое значение: Outlook не должно сканировать папки контактов в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

