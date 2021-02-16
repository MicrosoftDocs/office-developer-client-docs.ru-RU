---
title: Сведения об API управления учетными записями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'API управления учетной записью предоставляет доступ к сведениям об учетной записи и поддерживает уведомления об изменениях учетной записи. Как клиенты этого API поставщики почты делают следующее:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426251"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="8359c-104">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="8359c-104">About the Account Management API</span></span>

<span data-ttu-id="8359c-105">API управления учетной записью предоставляет доступ к сведениям об учетной записи и поддерживает уведомления об изменениях учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8359c-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="8359c-106">Как клиенты этого API поставщики почты делают следующее:</span><span class="sxs-lookup"><span data-stu-id="8359c-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="8359c-107">Управление доступом к учетным записям и настройка уведомлений об изменениях учетных записей с помощью [IOlkAccountManager.](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="8359c-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="8359c-108">Реализуйте и используйте [IOlkAccountNotify](iolkaccountnotify.md) для отправки уведомлений об изменениях учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8359c-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="8359c-109">Используйте [IOlkEnum для](iolkenum.md) нумерации учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8359c-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="8359c-110">Используйте [IOlkAccount](iolkaccount.md) для получения и применения свойств и других сведений об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8359c-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="8359c-111">Клиенты получают этот интерфейс через [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) или [IOlkEnum::GetNext](iolkenum-getnext.md) для доступа к отдельной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8359c-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="8359c-112">Реализация и использование [IOlkAccountHelper](iolkaccounthelper.md) для предоставления диспетчеру учетных записей дополнительных функций, включая получение имени профиля учетной записи и текущего сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="8359c-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="8359c-113">Реализуя и используйте [IOlkErrorUnknown,](iolkerrorunknown.md) чтобы предоставить дополнительные сведения об ошибке **в IOlkAccountManager,** **IOlkAccountNotify** и **IOlkAccount.**</span><span class="sxs-lookup"><span data-stu-id="8359c-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="8359c-114">Компоненты API управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="8359c-114">Account Management API components</span></span>

<span data-ttu-id="8359c-115">API управления учетной записью предоставляет следующие определения, типы данных, интерфейсы, именуемые свойства и свойства.</span><span class="sxs-lookup"><span data-stu-id="8359c-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="8359c-116">Определения</span><span class="sxs-lookup"><span data-stu-id="8359c-116">Definitions</span></span>
  
- [<span data-ttu-id="8359c-117">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="8359c-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="8359c-118">Типы данных</span><span class="sxs-lookup"><span data-stu-id="8359c-118">Data types</span></span>
  
- [<span data-ttu-id="8359c-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="8359c-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="8359c-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="8359c-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="8359c-121">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="8359c-121">Interfaces</span></span>
  
- [<span data-ttu-id="8359c-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="8359c-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="8359c-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="8359c-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="8359c-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="8359c-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="8359c-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="8359c-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="8359c-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="8359c-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="8359c-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="8359c-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="8359c-128">Именованные свойства</span><span class="sxs-lookup"><span data-stu-id="8359c-128">Named properties</span></span>
  
- [<span data-ttu-id="8359c-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="8359c-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="8359c-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="8359c-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="8359c-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="8359c-131">Properties</span></span>
  
- [<span data-ttu-id="8359c-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="8359c-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="8359c-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="8359c-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="8359c-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="8359c-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="8359c-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="8359c-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="8359c-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="8359c-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="8359c-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="8359c-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="8359c-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="8359c-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="8359c-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="8359c-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="8359c-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="8359c-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="8359c-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="8359c-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="8359c-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="8359c-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="8359c-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="8359c-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="8359c-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="8359c-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="8359c-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="8359c-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="8359c-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8359c-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="8359c-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8359c-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

