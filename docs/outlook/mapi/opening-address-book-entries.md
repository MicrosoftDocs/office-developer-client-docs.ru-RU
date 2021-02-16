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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422161"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="8482d-103">Открытие записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="8482d-103">Opening address book entries</span></span>

<span data-ttu-id="8482d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8482d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8482d-105">Когда клиент или поставщик запрашивает открытие одного из ваших объектов, MAPI вызывает метод [IABLogon::OpenEntry](iablogon-openentry.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="8482d-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="8482d-106">MAPI определяет, что идентификатор записи, представляющий целевой объект, принадлежит поставщику, изучив часть [MAPIUID](mapiuid.md) идентификатора записи и сопосмотрев ее с **MAPIUID,** зарегистрированным поставщиком в вызове **IMAPISupport::SetProviderUID.**</span><span class="sxs-lookup"><span data-stu-id="8482d-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="8482d-107">Затем MAPI вызывает метод **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="8482d-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="8482d-108">Поставщик должен ответить, запросив соответствующий объект — контейнер, список рассылки или пользователя системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8482d-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="8482d-109">Идентификатор записи NULL указывает запрос на открытие корневого контейнера поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="8482d-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="8482d-110">Клиенты открывают корневой контейнер, чтобы получить доступ к его таблице иерархии и ее получателям.</span><span class="sxs-lookup"><span data-stu-id="8482d-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="8482d-111">Поставщики адресных книг, которые только поставляют шаблоны для создания разных получателей, не поддерживают вызов **OpenEntry** для корневого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8482d-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="8482d-112">Реализация IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8482d-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="8482d-113">Убедитесь, что идентификатор записи является допустимым идентификатором, поддерживаемым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8482d-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="8482d-114">Если он не является допустимым идентификатором записи, MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="8482d-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="8482d-115">Проверьте флаг, переданный с помощью параметра _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8482d-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8482d-116">Если MAPI передан в MAPI_MODIFY поставщик не разрешает изменять его объекты, сбой и возврат значения ошибки MAPI_E_ACCESS_DENIED ошибки.</span><span class="sxs-lookup"><span data-stu-id="8482d-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="8482d-117">Убедитесь, что интерфейс, запрашиваемой в  _параметре lpInterface,_ действителен для типа объекта, который был предложен открыть поставщику.</span><span class="sxs-lookup"><span data-stu-id="8482d-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="8482d-118">Если передан недопустимый параметр, сбой и возврат MAPI_E_INTERFACE_NOT_SUPPORTED ошибки.</span><span class="sxs-lookup"><span data-stu-id="8482d-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="8482d-119">Если параметр  _cbEntryID имеет_ нулевое значение, это запрос на открытие корневого контейнера поставщика.</span><span class="sxs-lookup"><span data-stu-id="8482d-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="8482d-120">Создайте корневой контейнер и вернетесь указатель на реализацию интерфейса **IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="8482d-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="8482d-121">Если поставщик реализует несколько объектов входа, каждый из которых имеет собственный **зарегистрированный MAPIUID,** соединен **mapIUID,** содержащийся в идентификаторе записи, с соответствующим объектом входа.</span><span class="sxs-lookup"><span data-stu-id="8482d-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="8482d-122">Определите тип объекта, который представляет идентификатор записи: пользователь системы обмена сообщениями, список рассылки или контейнер, принадлежащий поставщику, или одноразовый пользователь или список рассылки сообщений, чтобы можно было установить соответствующее значение для параметра _lpulObjectType._</span><span class="sxs-lookup"><span data-stu-id="8482d-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="8482d-123">Создайте объект соответствующего типа и установите следующие базовые свойства:</span><span class="sxs-lookup"><span data-stu-id="8482d-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="8482d-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8482d-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="8482d-125">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8482d-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="8482d-126">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8482d-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="8482d-127">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8482d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="8482d-128">Вычисляет **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md) **и** PR_DISPLAY_NAME ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)из сведений в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="8482d-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="8482d-129">Возвращает указатель на реализацию интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="8482d-129">Return a pointer to the interface implementation for the object.</span></span> 
    

