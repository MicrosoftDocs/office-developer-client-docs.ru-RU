---
title: Открытие адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cd86b9cc86f30aac75b732b97208933de4d336e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566434"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="60779-103">Открытие адресной книги</span><span class="sxs-lookup"><span data-stu-id="60779-103">Opening address book entries</span></span>

<span data-ttu-id="60779-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60779-105">Когда клиента или поставщика запросил один из объектов открываются MAPI вызывает метод [IABLogon::OpenEntry](iablogon-openentry.md) ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="60779-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="60779-106">MAPI определяет, что запись идентификатор, представляющий целевой объект принадлежит к поставщику, проверяя [MAPIUID](mapiuid.md) часть идентификатор записи и сопоставление его **MAPIUID** , ваш поставщик зарегистрирован в вызове ** IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="60779-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="60779-107">MAPI вызывает метод **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="60779-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="60779-108">Поставщик должен отвечать путем получения соответствующего объекта — контейнер, список рассылки или обмена мгновенными сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="60779-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="60779-109">Идентификатор записи NULL указывает запрос для открытия контейнера корневым поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="60779-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="60779-110">Клиенты откройте корневой контейнер для доступа к таблице его иерархии и его получателей.</span><span class="sxs-lookup"><span data-stu-id="60779-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="60779-111">Поставщиками адресных книг, которые только предоставляют шаблоны для создания одноразовых получатели не поддерживают вызова **OpenEntry** для корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="60779-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="60779-112">Для реализации IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="60779-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="60779-113">Убедитесь, что идентификатор записи допустимый идентификатор, ваш поставщик поддерживает.</span><span class="sxs-lookup"><span data-stu-id="60779-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="60779-114">Если не является допустимым идентификатором, возвратите MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="60779-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="60779-115">Проверьте флаг, который передается с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="60779-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="60779-116">Если истекло MAPI в MAPI_MODIFY и ваш поставщик не позволяет его объекты, которую нужно изменить, давать сбой и возвращать значение MAPI_E_ACCESS_DENIED ошибки.</span><span class="sxs-lookup"><span data-stu-id="60779-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="60779-117">Убедитесь, что на интерфейс, запрошенный в параметре _lpInterface_ допустимый тип объекта, который запросил у поставщика для открытия.</span><span class="sxs-lookup"><span data-stu-id="60779-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="60779-118">Если переданную недопустимый параметр давать сбой и возвращать значение MAPI_E_INTERFACE_NOT_SUPPORTED ошибки.</span><span class="sxs-lookup"><span data-stu-id="60779-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="60779-119">Если параметр _cbEntryID_ равно нулю, это запроса на открытие ваш поставщик корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="60779-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="60779-120">Создание корневого контейнера и возвращает указатель на его реализация интерфейса **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="60779-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="60779-121">Если ваш поставщик реализует несколько объектов входа в систему, каждый со своим зарегистрирован **MAPIUID**, карты **MAPIUID** содержащимися в идентификатор записи с помощью объекта соответствующие входа в систему.</span><span class="sxs-lookup"><span data-stu-id="60779-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="60779-122">Определить, какой тип объекта представляет идентификатор записи: обмена сообщениями пользователя, список рассылки или контейнера, относящегося к поставщику или одноразовых обмена сообщениями пользователя или список рассылки, соответствующее значение можно использовать для _lpulObjectType_ параметр.</span><span class="sxs-lookup"><span data-stu-id="60779-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="60779-123">Создание объекта соответствующего типа и задайте следующие основные свойства:</span><span class="sxs-lookup"><span data-stu-id="60779-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="60779-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60779-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="60779-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60779-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="60779-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60779-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="60779-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60779-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="60779-128">Вычисление **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) на основании сведений в идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="60779-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="60779-129">Возвращает указатель для реализации интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="60779-129">Return a pointer to the interface implementation for the object.</span></span> 
    

