---
title: Решение имени получателя
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
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="b10c5-103">Решение имени получателя</span><span class="sxs-lookup"><span data-stu-id="b10c5-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="b10c5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b10c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b10c5-105">Когда сообщение адресовано, список получателей строится со свойствами, связанными с каждым получателем.</span><span class="sxs-lookup"><span data-stu-id="b10c5-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="b10c5-106">К моменту отправления сообщения одним из этих свойств должен быть долгосрочный идентификатор входа получателя.</span><span class="sxs-lookup"><span data-stu-id="b10c5-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="b10c5-107">Чтобы убедиться, что **каждый получатель** включает свойство [PR_ENTRYID (PidTagEntryId),](pidtagentryid-canonical-property.md)передайте структуру [ADRLIST,](adrlist.md) описывая список получателей в содержимом параметра  _lpAdrList_ в вызове [в IAddrBook::ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="b10c5-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="b10c5-108">**ResolveName** начинает обработку, игнорируя уже разрешенные записи в структуре **ADRLIST,** о чем свидетельствует наличие идентификатора записи в массиве **SPropValue** соответствующей структуры [ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="b10c5-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="b10c5-109">Далее **ResolveName** автоматически назначает идентификаторы разовой записи двум типам получателей:</span><span class="sxs-lookup"><span data-stu-id="b10c5-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="b10c5-110">Получатели с адресом, отформатированный в виде интернет-адреса</span><span class="sxs-lookup"><span data-stu-id="b10c5-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="b10c5-111">Получатели с адресом, отформатированные следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b10c5-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="b10c5-112">Для всех оставшихся записей **ResolveName** ищет адресную книгу для точного совпадения на отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="b10c5-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="b10c5-113">**ResolveName** **использует свойство PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)для определения набора контейнеров для поиска и порядка поиска.</span><span class="sxs-lookup"><span data-stu-id="b10c5-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="b10c5-114">MAPI вызывает [метод IABContainer::ResolveNames](iabcontainer-resolvenames.md) каждого контейнера, чтобы попытаться устранить все имена.</span><span class="sxs-lookup"><span data-stu-id="b10c5-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="b10c5-115">Так как некоторые контейнеры не поддерживают **ResolveNames,** если контейнер возвращается  MAPI_E_NO_SUPPORT, MAPI применяет ограничение свойств PR_ANR [(PidTagAnr)](pidtaganr-canonical-property.md)к его таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="b10c5-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="b10c5-116">Все контейнеры адресной книги необходимы для поддержки разрешения имен с помощью этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="b10c5-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="b10c5-117">После того, как все имена будут устранены, дополнительные вызовы контейнеров не будут сделаны.</span><span class="sxs-lookup"><span data-stu-id="b10c5-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="b10c5-118">Если все контейнеры были вызваны, но остаются неоднозначные или неурегулированные имена, MAPI отображает диалоговое окно, если это возможно, чтобы побудить пользователя разрешить оставшиеся имена.</span><span class="sxs-lookup"><span data-stu-id="b10c5-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="b10c5-119">Ограничение **PR_ANR** соответствует значению свойства  PR_ANR имени отображения в **структуре ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="b10c5-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="b10c5-120">Ограничение представления таблицы содержимого контейнера с  ограничением свойств PR_ANR позволяет поставщику адресной книги выполнять поиск по "наилучшему угадайку", совпадая с свойством, которое имеет смысл для поставщика.</span><span class="sxs-lookup"><span data-stu-id="b10c5-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="b10c5-121">Например, один поставщик адресных книг может всегда соответствовать именам в списке получателей **PR_DISPLAY_NAME** [(PidTagDisplayName),](pidtagdisplayname-canonical-property.md)а другой может разрешить администратору выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="b10c5-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="b10c5-122">**Установить ограничение PR_ANR свойств в таблице содержимого контейнера адресной книги**</span><span class="sxs-lookup"><span data-stu-id="b10c5-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="b10c5-123">Создайте [структуру SRestriction,](srestriction.md) как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="b10c5-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="b10c5-124">Вызов метода [IMAPITable:::Restrict](imapitable-restrict.md) таблицы содержимого, передав структуру **SRestriction** в качестве _параметра lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="b10c5-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

