---
title: Разрешение имя получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812138"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="6723d-103">Разрешение имя получателя</span><span class="sxs-lookup"><span data-stu-id="6723d-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="6723d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6723d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6723d-105">Когда сообщение можно решить, список получателей построения со свойствами, относящиеся к каждому получателю.</span><span class="sxs-lookup"><span data-stu-id="6723d-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="6723d-106">С момента отправки сообщения один из этих свойств должен быть долгосрочного запись идентификатор получателя.</span><span class="sxs-lookup"><span data-stu-id="6723d-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="6723d-107">Чтобы убедиться, что для каждого получателя, содержит свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), передайте [ADRLIST](adrlist.md) структуры, описывающие список получателей в содержимое параметра _lpAdrList_ к вызову [IAddrBook:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="6723d-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="6723d-108">**ResolveName** начинает обработку, игнорируя записи в структуре **ADRLIST** , которые уже разрешены, как указано в присутствия идентификатор записи в соответствующем структура [ADRENTRY](adrentry.md) **SPropValue** массив.</span><span class="sxs-lookup"><span data-stu-id="6723d-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="6723d-109">Рассмотрим процедуру **ResolveName** автоматически устанавливает идентификаторы единичных записей для двух типов получателей:</span><span class="sxs-lookup"><span data-stu-id="6723d-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="6723d-110">Получатели с адресом в формате адреса в Интернете</span><span class="sxs-lookup"><span data-stu-id="6723d-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="6723d-111">Получатели с адресом следующий формат:</span><span class="sxs-lookup"><span data-stu-id="6723d-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="6723d-112">Для всех остальных записей **ResolveName** поиск точного совпадения на отображаемое имя в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="6723d-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="6723d-113">**ResolveName** использует свойство **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) для определения набора контейнеров для поиска и порядок поиска.</span><span class="sxs-lookup"><span data-stu-id="6723d-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="6723d-114">MAPI вызывает метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) каждые контейнера, чтобы разрешить всем именам.</span><span class="sxs-lookup"><span data-stu-id="6723d-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="6723d-115">Так как некоторые контейнеров не поддерживают **ResolveNames**, если контейнер возвращает MAPI_E_NO_SUPPORT, MAPI применяется ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) от его содержимое в таблице.</span><span class="sxs-lookup"><span data-stu-id="6723d-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="6723d-116">Все контейнеры адресной книги требуются для поддержки разрешение имен с это ограничение.</span><span class="sxs-lookup"><span data-stu-id="6723d-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="6723d-117">Когда все имена разрешаются, больше не контейнер вызовы выполняются.</span><span class="sxs-lookup"><span data-stu-id="6723d-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="6723d-118">Вызвали контейнеров, но остаются неоднозначные или нерешенные имена, MAPI отображает диалоговое окно, если это возможно пригласить пользователя для разрешения имен остальных.</span><span class="sxs-lookup"><span data-stu-id="6723d-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="6723d-119">Ограничение **PR_ANR** совпадает со значением свойства **PR_ANR** относительно отображаемое имя в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="6723d-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="6723d-120">Ограничение представление таблицы содержимого контейнера с ограничением свойство **PR_ANR** вызывает поставщик адресной книги для выполнения «лучше всего подбора» тип поиска, сравнение с свойство, которое имеет смысл для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6723d-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="6723d-121">Например один поставщик адресной книги всегда может совпадать имена в список получателей с **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), в то время как другой может позволить администратору выбрать свойство.</span><span class="sxs-lookup"><span data-stu-id="6723d-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="6723d-122">**Чтобы задать ограничение свойства PR_ANR на таблицу содержимого контейнер адресной книги**</span><span class="sxs-lookup"><span data-stu-id="6723d-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="6723d-123">Создание структуры [SRestriction](srestriction.md) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="6723d-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="6723d-124">Вызовите метод [IMAPITable::Restrict](imapitable-restrict.md) таблицы, передачи структуры **SRestriction** в качестве параметра _lpRestriction_ содержимое.</span><span class="sxs-lookup"><span data-stu-id="6723d-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

