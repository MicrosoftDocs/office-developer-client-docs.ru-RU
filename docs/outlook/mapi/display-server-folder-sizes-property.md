---
title: Отображение свойства размеров папок сервера
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337081"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="d2865-103">Отображение свойства размеров папок сервера</span><span class="sxs-lookup"><span data-stu-id="d2865-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="d2865-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2865-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2865-105">Отображает размеры указанных папок на сервере в диалоговом окне **Размер папки** Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2865-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d2865-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d2865-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2865-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="d2865-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="d2865-108">[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d2865-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="d2865-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="d2865-109">Created by:</span></span>  <br/> |<span data-ttu-id="d2865-110">Поставщик хранилища</span><span class="sxs-lookup"><span data-stu-id="d2865-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="d2865-111">Доступ:</span><span class="sxs-lookup"><span data-stu-id="d2865-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="d2865-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="d2865-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="d2865-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="d2865-113">Property type:</span></span>  <br/> |<span data-ttu-id="d2865-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d2865-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d2865-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="d2865-115">Access type:</span></span>  <br/> |<span data-ttu-id="d2865-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d2865-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2865-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2865-117">Remarks</span></span>

<span data-ttu-id="d2865-118">Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMAPIProp: IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданного в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="d2865-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="d2865-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::](imapiprop-getprops.md)-Props, поставщик хранилища также должен возвращать правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="d2865-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="d2865-120">Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств.</span><span class="sxs-lookup"><span data-stu-id="d2865-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="d2865-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="d2865-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="d2865-122">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="d2865-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2865-123">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="d2865-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="d2865-124">ПС_ПУБЛИК_СТРИНГС</span><span class="sxs-lookup"><span data-stu-id="d2865-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="d2865-125">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="d2865-125">ulKind:</span></span>  <br/> |<span data-ttu-id="d2865-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d2865-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="d2865-127">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="d2865-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="d2865-128">L "urn: schemas-microsoft-com: Office: Outlook # серверфолдерсизес"</span><span class="sxs-lookup"><span data-stu-id="d2865-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="d2865-129">Это свойство поддерживается в Microsoft Outlook 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d2865-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="d2865-130">Если версия Outlook более ранняя, чем Outlook 2003 с ПАКЕТом обновления 1 (SP1), или если его значение равно **false**, в Outlook будут отображаться только размеры папок в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="d2865-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="d2865-131">Если это свойство задано для хранилища, использующего Outlook 2003 с ПАКЕТом обновления 1 (SP1), Outlook запросит размер каждой указанной папки на сервере и на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="d2865-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="d2865-132">Чтобы запросить размер папки на сервере, Outlook открывает папку в хранилище с [IMsgStore:: OpenEntry](imsgstore-openentry.md), передавая флаг **мапи_но_каче**, а затем отправляет запрос на **пр_мессаже_сизе_екстендед**.</span><span class="sxs-lookup"><span data-stu-id="d2865-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="d2865-133">Поставщик услуг хранения должен возвратить размер папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="d2865-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="d2865-134">Чтобы запросить размер папки на локальном диске, Outlook открывает папку без флага **мапи_но_каче** .</span><span class="sxs-lookup"><span data-stu-id="d2865-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="d2865-135">Затем он запрашивает **пр_мессаже_сизе_екстендед**; поставщик хранилища должен возвратить размер указанной папки на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="d2865-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="d2865-136">Если это свойство задано, поставщики хранилища, которые синхронизируют содержимое хранилища с сервером, могут отображать данные о размере папки на сервере в диалоговом окне **Размер папки** Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2865-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="d2865-137">Затем пользователи могут сравнить текущее использование хранилища серверов с серверными квотами.</span><span class="sxs-lookup"><span data-stu-id="d2865-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

