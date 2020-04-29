---
title: Разрешение имени получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405868"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="9045b-103">Разрешение имени получателя</span><span class="sxs-lookup"><span data-stu-id="9045b-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="9045b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9045b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9045b-105">При отправке сообщения список получателей строится со свойствами, связанными с каждым получателем.</span><span class="sxs-lookup"><span data-stu-id="9045b-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="9045b-106">К моменту отправки сообщения одно из этих свойств должно быть идентификатором долгосрочного входа получателя.</span><span class="sxs-lookup"><span data-stu-id="9045b-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="9045b-107">Чтобы убедиться, что каждый получатель включает свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), передайте структуру [ADRLIST](adrlist.md) , описывающую список получателей, в содержимое параметра _Лпадрлист_ в вызове [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="9045b-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="9045b-108">**Ресолвенаме** начинает обработку, игнорируя записи в структуре **ADRLIST** , которые уже были разрешены, как указано в элементе идентификатора записи в соответствующем массиве **спропвалуе** структуры [адрентри](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="9045b-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="9045b-109">После этого **ресолвенаме** автоматически назначит одноразовые идентификаторы записей двум типам получателей:</span><span class="sxs-lookup"><span data-stu-id="9045b-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="9045b-110">Получатели с адресом, отформатированным в виде адреса в Интернете</span><span class="sxs-lookup"><span data-stu-id="9045b-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="9045b-111">Получатели с адресом, отформатированным следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9045b-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="9045b-112">Для всех оставшихся записей **ресолвенаме** ищет точное совпадение с отображаемым именем в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="9045b-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="9045b-113">**Ресолвенаме** использует свойство **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), чтобы определить набор контейнеров для поиска и порядок поиска.</span><span class="sxs-lookup"><span data-stu-id="9045b-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="9045b-114">MAPI вызывает метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) каждого контейнера, чтобы попытаться разрешить все имена.</span><span class="sxs-lookup"><span data-stu-id="9045b-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="9045b-115">Так как некоторые контейнеры не поддерживают **ResolveNames**, если контейнер возвращает MAPI_E_NO_SUPPORT, MAPI применяет ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) к своей таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="9045b-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="9045b-116">Все контейнеры адресной книги должны поддерживать разрешение имен с использованием этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="9045b-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="9045b-117">После того как все имена будут устранены, дальнейшие вызовы контейнеров не выполняются.</span><span class="sxs-lookup"><span data-stu-id="9045b-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="9045b-118">Если все контейнеры были вызваны, но при этом остаются неоднозначные или неразрешенные имена, MAPI отображает диалоговое окно, если возможно запросить разрешение пользователя на разрешение оставшихся имен.</span><span class="sxs-lookup"><span data-stu-id="9045b-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="9045b-119">Ограничение **PR_ANR** сопоставляет значение свойства **PR_ANR** с отображаемым именем в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9045b-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="9045b-120">Ограничение представления таблицы содержимого контейнера с помощью ограничения свойства **PR_ANR** приводит к тому, что поставщику адресной книги требуется тип поиска, соответствующий свойству, которое имеет смысл для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9045b-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="9045b-121">Например, один поставщик адресных книг может всегда сопоставлять имена в списке получателей с **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), в то время как другой может позволить администратору выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="9045b-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="9045b-122">**Настройка ограничения свойства PR_ANR для таблицы содержимого контейнера адресной книги**</span><span class="sxs-lookup"><span data-stu-id="9045b-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="9045b-123">Создайте структуру [срестриктион](srestriction.md) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="9045b-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="9045b-124">Вызовите для таблицы содержаний метод [IMAPITable:: restrict](imapitable-restrict.md) , передав структуру **срестриктион** в качестве параметра _лпрестриктион_ .</span><span class="sxs-lookup"><span data-stu-id="9045b-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

