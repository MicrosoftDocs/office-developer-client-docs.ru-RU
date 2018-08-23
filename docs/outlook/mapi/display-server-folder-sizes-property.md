---
title: Свойство отображения размеров папок на сервере
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
ms.openlocfilehash: f1ec10bde39f853a80540b48216478edc4e41f12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584312"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="92c09-103">Свойство отображения размеров папок на сервере</span><span class="sxs-lookup"><span data-stu-id="92c09-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="92c09-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92c09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92c09-105">Отображает размеры указанных папках на сервере в диалоговом окне Outlook **Размер папки** .</span><span class="sxs-lookup"><span data-stu-id="92c09-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="92c09-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="92c09-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92c09-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="92c09-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="92c09-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="92c09-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="92c09-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="92c09-109">Created by:</span></span>  <br/> |<span data-ttu-id="92c09-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="92c09-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="92c09-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="92c09-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="92c09-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="92c09-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="92c09-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="92c09-113">Property type:</span></span>  <br/> |<span data-ttu-id="92c09-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="92c09-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="92c09-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="92c09-115">Access type:</span></span>  <br/> |<span data-ttu-id="92c09-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="92c09-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92c09-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="92c09-117">Remarks</span></span>

<span data-ttu-id="92c09-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="92c09-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="92c09-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="92c09-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="92c09-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="92c09-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="92c09-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="92c09-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="92c09-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="92c09-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92c09-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="92c09-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="92c09-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="92c09-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="92c09-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="92c09-125">ulKind:</span></span>  <br/> |<span data-ttu-id="92c09-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="92c09-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="92c09-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="92c09-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="92c09-128">L "urn: schemas-microsoft-com:office:outlook #serverfoldersizes»</span><span class="sxs-lookup"><span data-stu-id="92c09-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="92c09-129">Это свойство поддерживается в Microsoft Outlook 2003 с пакетом обновления (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="92c09-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="92c09-130">Если используется Outlook версии более ранней, чем Outlook 2003 пакет обновления 1 или имеет значение **false**, Outlook будут отображаться только размеры папок локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="92c09-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="92c09-131">Если это свойство задано для хранилища, который использует Outlook 2003 SP 1, Outlook будет запрашивать размер каждой указанной папке на локальном диске и серверы.</span><span class="sxs-lookup"><span data-stu-id="92c09-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="92c09-132">Для отправки запросов о размер папки на сервере, Outlook откроется в папку на хранилище с [IMsgStore::OpenEntry](imsgstore-openentry.md), передав флаг **MAPI_NO_CACHE**, и затем отправляет запрос для **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="92c09-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="92c09-133">Затем поставщик хранения должен возвращать размер папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="92c09-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="92c09-134">Чтобы запросить размер в папку на локальном диске, Outlook откроется в папку без флага **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="92c09-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="92c09-135">Он затем выполняется запрос **PR_MESSAGE_SIZE_EXTENDED**; поставщик хранения должен возвращать размер указанную папку на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="92c09-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="92c09-136">С помощью этого набора свойств поставщики хранилища, синхронизировать содержимое хранилища на сервере можно отобразить данных размер папки на сервере в диалоговом окне Outlook **Размер папки** .</span><span class="sxs-lookup"><span data-stu-id="92c09-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="92c09-137">Пользователи могут сравнить их текущего использования хранилища сервера с квоты сервера.</span><span class="sxs-lookup"><span data-stu-id="92c09-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

