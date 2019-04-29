---
title: Сведения об API управления учетными записями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях в учетной записи. Как клиенты этого API, поставщики почты выполняют следующие действия:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426251"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="2fdfa-104">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="2fdfa-104">About the Account Management API</span></span>

<span data-ttu-id="2fdfa-105">API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="2fdfa-106">Как клиенты этого API, поставщики почты выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2fdfa-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="2fdfa-107">Используйте [иолкаккаунтманажер](iolkaccountmanager.md) для управления доступом к учетным записям и настройки уведомлений об изменениях учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="2fdfa-108">Реализация и использование [иолкаккаунтнотифи](iolkaccountnotify.md) для отправки уведомлений об изменениях учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="2fdfa-109">Используйте [иолкенум](iolkenum.md) для перечисления учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="2fdfa-110">Используйте [иолкаккаунт](iolkaccount.md) для получения и задания свойств и других сведений об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="2fdfa-111">Клиенты получают этот интерфейс с помощью [иолкаккаунтманажер:: финдаккаунт](iolkaccountmanager-findaccount.md) или [Иолкенум:: GetNext](iolkenum-getnext.md) для доступа к отдельной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="2fdfa-112">Реализуйте и используйте [иолкаккаунселпер](iolkaccounthelper.md) для предоставления вспомогательных функций диспетчера учетных записей, включая извлечение имени профиля учетной записи и текущего сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="2fdfa-113">Реализуйте и используйте [иолкеррорункновн](iolkerrorunknown.md) , чтобы предоставить дополнительные сведения об ошибке в **иолкаккаунтманажер**, **иолкаккаунтнотифи**и **иолкаккаунт**.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="2fdfa-114">Компоненты API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="2fdfa-114">Account Management API components</span></span>

<span data-ttu-id="2fdfa-115">API управления учетными записями предоставляет следующие определения, типы данных, интерфейсы, именованные свойства и свойства.</span><span class="sxs-lookup"><span data-stu-id="2fdfa-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="2fdfa-116">Определения</span><span class="sxs-lookup"><span data-stu-id="2fdfa-116">Definitions</span></span>
  
- [<span data-ttu-id="2fdfa-117">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="2fdfa-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="2fdfa-118">Типы данных</span><span class="sxs-lookup"><span data-stu-id="2fdfa-118">Data types</span></span>
  
- [<span data-ttu-id="2fdfa-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="2fdfa-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="2fdfa-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="2fdfa-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="2fdfa-121">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="2fdfa-121">Interfaces</span></span>
  
- [<span data-ttu-id="2fdfa-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="2fdfa-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="2fdfa-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="2fdfa-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="2fdfa-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="2fdfa-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="2fdfa-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="2fdfa-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="2fdfa-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="2fdfa-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="2fdfa-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="2fdfa-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="2fdfa-128">Именованные свойства</span><span class="sxs-lookup"><span data-stu-id="2fdfa-128">Named properties</span></span>
  
- [<span data-ttu-id="2fdfa-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="2fdfa-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="2fdfa-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="2fdfa-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="2fdfa-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="2fdfa-131">Properties</span></span>
  
- [<span data-ttu-id="2fdfa-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="2fdfa-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="2fdfa-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2fdfa-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="2fdfa-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="2fdfa-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="2fdfa-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="2fdfa-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="2fdfa-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="2fdfa-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="2fdfa-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="2fdfa-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="2fdfa-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="2fdfa-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="2fdfa-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="2fdfa-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="2fdfa-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="2fdfa-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="2fdfa-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="2fdfa-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="2fdfa-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="2fdfa-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="2fdfa-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="2fdfa-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="2fdfa-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="2fdfa-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="2fdfa-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="2fdfa-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="2fdfa-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2fdfa-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="2fdfa-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2fdfa-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

