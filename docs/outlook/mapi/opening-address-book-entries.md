---
title: Открытие записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326329"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="f208f-103">Открытие записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="f208f-103">Opening address book entries</span></span>

<span data-ttu-id="f208f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f208f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f208f-105">Когда клиент или поставщик запросили открыть один из объектов, MAPI вызывает метод [иаблогон:: OpenEntry](iablogon-openentry.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="f208f-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="f208f-106">MAPI определяет, что идентификатор записи, представляющий целевой объект, принадлежит поставщику, изучая часть [мапиуид](mapiuid.md) идентификатора записи и сопоставляя его с **мапиуид** , зарегистрированным в вызове **. Имаписуппорт:: Сетпровидеруид**.</span><span class="sxs-lookup"><span data-stu-id="f208f-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="f208f-107">Затем MAPI вызывает метод **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="f208f-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="f208f-108">Поставщик должен ответить, получая соответствующий объект — контейнер, список рассылки или пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f208f-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="f208f-109">Идентификатор записи NULL указывает на запрос на открытие корневого контейнера поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f208f-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="f208f-110">Клиенты открывают корневой контейнер для доступа к своей таблице иерархии и его получателям.</span><span class="sxs-lookup"><span data-stu-id="f208f-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="f208f-111">Поставщики адресных книг, которые предоставляют только шаблоны для создания одноразовых получателей, не поддерживают вызов **OpenEntry** для корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="f208f-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="f208f-112">Реализация Иаблогон:: OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f208f-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="f208f-113">Убедитесь, что идентификатор записи является допустимым идентификатором, поддерживаемым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f208f-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="f208f-114">Если он не является допустимым идентификатором записи, возвращается МАПИ_Е_ИНВАЛИД_ЕНТРИД.</span><span class="sxs-lookup"><span data-stu-id="f208f-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f208f-115">Проверьте флаг, который передается с параметром _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f208f-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f208f-116">Если MAPI передается в МАПИ_МОДИФИ, а ваш поставщик не позволяет изменять его объекты, завершится с ошибкой и возвратите значение ошибки МАПИ_Е_АКЦЕСС_ДЕНИЕД.</span><span class="sxs-lookup"><span data-stu-id="f208f-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="f208f-117">Убедитесь, что интерфейс, запрашиваемый в параметре _лпинтерфаце_ , действителен для типа объекта, который запросил открыть поставщик.</span><span class="sxs-lookup"><span data-stu-id="f208f-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="f208f-118">Если передается недопустимый параметр, происходит сбой и возвращается значение ошибки МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД.</span><span class="sxs-lookup"><span data-stu-id="f208f-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="f208f-119">Если параметр _кбентрид_ равен нулю, это запрос на открытие корневого контейнера поставщика.</span><span class="sxs-lookup"><span data-stu-id="f208f-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="f208f-120">Создайте корневой контейнер и возвратите указатель на его реализацию интерфейса **иабконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="f208f-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="f208f-121">Если поставщик реализует несколько объектов входа, каждый со своим зарегистрированным **мапиуид**, сопоставьте **мапиуид** , содержащиеся в идентификаторе записи, с соответствующим объектом logon.</span><span class="sxs-lookup"><span data-stu-id="f208f-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="f208f-122">Определите тип объекта, представленный идентификатором записи: пользователь обмена сообщениями, список рассылки или контейнер, принадлежащий поставщику или одноразовому пользователю обмена сообщениями, чтобы можно было установить соответствующее значение для _лпулобжекттипе_ . параметр.</span><span class="sxs-lookup"><span data-stu-id="f208f-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="f208f-123">Создайте объект соответствующего типа и задайте следующие основные свойства:</span><span class="sxs-lookup"><span data-stu-id="f208f-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="f208f-124">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f208f-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="f208f-125">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f208f-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="f208f-126">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f208f-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="f208f-127">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f208f-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="f208f-128">ВыЧислите **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) из сведений в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="f208f-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="f208f-129">Возвращает указатель на реализацию интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="f208f-129">Return a pointer to the interface implementation for the object.</span></span> 
    

