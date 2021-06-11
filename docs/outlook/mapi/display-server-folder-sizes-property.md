---
title: Свойство Display Server Folder Sizes
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434552"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="710c2-103">Свойство Display Server Folder Sizes</span><span class="sxs-lookup"><span data-stu-id="710c2-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="710c2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="710c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="710c2-105">Отображает размеры указанных папок на сервере в  диалоговом окне Outlook размера папок.</span><span class="sxs-lookup"><span data-stu-id="710c2-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="710c2-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="710c2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="710c2-107">Выставлено на:</span><span class="sxs-lookup"><span data-stu-id="710c2-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="710c2-108">[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="710c2-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="710c2-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="710c2-109">Created by:</span></span>  <br/> |<span data-ttu-id="710c2-110">Поставщик магазинов</span><span class="sxs-lookup"><span data-stu-id="710c2-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="710c2-111">Доступ к ним:</span><span class="sxs-lookup"><span data-stu-id="710c2-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="710c2-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="710c2-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="710c2-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="710c2-113">Property type:</span></span>  <br/> |<span data-ttu-id="710c2-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="710c2-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="710c2-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="710c2-115">Access type:</span></span>  <br/> |<span data-ttu-id="710c2-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="710c2-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="710c2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="710c2-117">Remarks</span></span>

<span data-ttu-id="710c2-118">Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="710c2-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="710c2-119">Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="710c2-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="710c2-120">Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="710c2-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="710c2-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="710c2-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="710c2-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="710c2-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="710c2-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="710c2-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="710c2-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="710c2-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="710c2-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="710c2-125">ulKind:</span></span>  <br/> |<span data-ttu-id="710c2-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="710c2-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="710c2-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="710c2-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="710c2-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="710c2-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="710c2-129">Это свойство поддерживается в Microsoft Outlook 2003 Пакет обновления (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="710c2-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="710c2-130">Если версия Outlook более Outlook 2003 SP 1 или если ее значение является ложным, Outlook отображает только размеры папок в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="710c2-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="710c2-131">Если это свойство установлено в магазине с Outlook 2003 SP 1, Outlook запрашивает размер каждой указанной папки на сервере и локальном диске.</span><span class="sxs-lookup"><span data-stu-id="710c2-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="710c2-132">Чтобы запросить размер папки на сервере, Outlook открывает папку в магазине [с помощью IMsgStore::OpenEntry,](imsgstore-openentry.md)передает флаг **MAPI_NO_CACHE,** а затем запрашивает PR_MESSAGE_SIZE_EXTENDED **.**</span><span class="sxs-lookup"><span data-stu-id="710c2-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="710c2-133">Затем поставщик магазина должен вернуть размер папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="710c2-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="710c2-134">Чтобы запросить размер папки на локальном диске, Outlook открывает папку без **MAPI_NO_CACHE** флага.</span><span class="sxs-lookup"><span data-stu-id="710c2-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="710c2-135">Затем он запрашивает **PR_MESSAGE_SIZE_EXTENDED;** поставщик магазина должен вернуть размер указанной папки на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="710c2-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="710c2-136">С помощью этого набора свойств поставщики магазинов, синхронизируются содержимое магазина с сервером, могут отображать данные о размере папок на сервере в диалоговом **окне** Outlook размера папки.</span><span class="sxs-lookup"><span data-stu-id="710c2-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="710c2-137">Пользователи могут сравнить текущее использование хранилища серверов с квотами серверов.</span><span class="sxs-lookup"><span data-stu-id="710c2-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

