---
title: Использование нескольких учетных записей Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329655"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="f89ea-103">Использование нескольких учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="f89ea-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="f89ea-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f89ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f89ea-105">Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживают интеграцию с несколькими учетными записями электронной почты Exchange.</span><span class="sxs-lookup"><span data-stu-id="f89ea-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange e-mail accounts.</span></span> <span data-ttu-id="f89ea-106">В Outlook 2010 и Outlook 2013 пользователь может добавить две учетные записи Exchange в один профиль, по-прежнему используя широкие возможности Exchange, такие как опубликованный глобальный список адресов (GAL), конфигурация отсутствия на рабочем месте в Exchange и общий доступ к папкам.</span><span class="sxs-lookup"><span data-stu-id="f89ea-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="f89ea-107">Те, кто знаком с разделами профиля MAPI для Microsoft Office Outlook 2007 и более ранних версий, знают, что параметры Exchange, такие как имя пользователя электронной почты и имя сервера, хранятся в фиксированном разделе глобального профиля Exchange — **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the e-mail user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="f89ea-108">В Outlook 2010 и Outlook 2013 каждой учетной записи Exchange требуется собственный раздел профиля для хранения параметров, что избавляет от необходимости в **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="f89ea-p103">Параметры Exchange в Outlook 2010 и Outlook 2013 по-прежнему хранятся в профиле, но уникальный идентификатор раздела профиля, содержащего эти параметры, динамически выделяется для каждого профиля. Расположение параметров Exchange в профиле указывается в свойстве [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), которое можно найти в разделе профиля службы сообщений для учетной записи Exchange. Это свойство также можно найти в разделе профиля для каждого поставщика в этой службе сообщений для учетной записи. Уникальный идентификатор не хранится на сервере и отличается от профиля к профилю.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="f89ea-p104">Outlook 2010 и Outlook 2013 используют **PidTagExchangeProfileSectionId** в качестве уникального идентификатора для указания учетной записи Exchange. При таком использовании этот уникальный идентификатор называется **emsmdbUID**. Для некоторых операций MAPI и Outlook идентификатор **emsmdbUID** может быть необходим, чтобы указать учетную запись Exchange, которую следует использовать для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="f89ea-p105">Для поддержки нескольких учетных записей Exchange необходимо использовать вызовы новых функций в коде. Замените любой вызов с использованием идентификатора **entryID** и метода [IAddrBook::OpenEntry](iaddrbook-openentry.md) или [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) в объектах [IMailUser : IMAPIProp](imailuserimapiprop.md) и [IDistList : IMAPIContainer](idistlistimapicontainer.md) одной из перечисленных ниже функций.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="f89ea-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="f89ea-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="f89ea-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="f89ea-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="f89ea-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="f89ea-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="f89ea-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="f89ea-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="f89ea-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="f89ea-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="f89ea-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="f89ea-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f89ea-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="f89ea-128">Поддержка старых версий</span><span class="sxs-lookup"><span data-stu-id="f89ea-128">Legacy support</span></span>

<span data-ttu-id="f89ea-p106">Все клиенты MAPI, написанные до создания нового раздела **emsmdbUID**, по-прежнему поддерживаются. Эти клиенты продолжат получать старый глобальный раздел **pbGlobalProfileSectionGuid**. Запросы для этого раздела профиля будут перенаправляться в одну выделенную учетную запись Exchange, обрабатывающую старые запросы. Учетную запись, которая обрабатывает старые вызовы, можно определить, сверившись с таблицей служб сообщений и добавив столбец для PR_EMSMDB_LEGACY. Только в одной службе сообщений для этого свойства будет задано значение true, а его свойству **PidTagExchangeProfileSectionId** присваивается значение старого идентификатора **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f89ea-p107">Настраиваемые параметры MAPI, такие как используемые по умолчанию хранилище и учетная запись, не влияют на то, какая учетная запись обрабатывает старые вызовы. Учетную запись, обрабатывающую старые вызовы, невозможно настроить.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="f89ea-p108">Свойство **emsmdbUID** старой учетной записи копируется в раздел глобального профиля Outlook. Если это свойство не существует, то с помощью таблицы служб сообщений можно определить, какая учетная запись обрабатывает старые запросы, и задать соответствующее значение в разделе глобального профиля Outlook.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="f89ea-p109">Для ясности, раздел глобального профиля Outlook отличается от аналогичного раздела в Exchange, а в Outlook 2010 и Outlook 2013 раздел глобального профиля Exchange больше не будет по-настоящему глобальным, так как у вас может быть несколько учетных записей Exchange. Раздел глобального профиля Outlook содержит свойства для Outlook, такие как состояние MRU папки или состояние глобального подключения.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="f89ea-140">Контексты учетных записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="f89ea-140">Address Book Account Contexts</span></span>

<span data-ttu-id="f89ea-141">Чтобы правильно разрешать адреса с несколькими учетными записями Exchange, используйте новые функции, принимающие контекст учетной записи, чтобы при вызове адресной книги выполнялся поиск в правильной учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="f89ea-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="f89ea-p110">Некоторые API адресной книги из предыдущих версий объявлены нерекомендуемыми, так как они не полностью поддерживали использование нескольких учетных записей Exchange. Как правило, этот контекст учетной записи представляется с помощью **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="f89ea-144">Помимо **emsmdbUID**, у нескольких учетных записей Exchange также есть **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="f89ea-145">Значение **emsmdbUID** определяет контекст учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f89ea-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="f89ea-146">Значение **emsabpUID** определяет поставщика адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="f89ea-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="f89ea-p111">Значение **emsabpUID** обычно используется при разрешении получателя. При разрешении получателя с помощью [IAddrBook::ResolveName](iaddrbook-resolvename.md) строка получателя Exchange содержит свойство **PR_AB_PROVIDERS** (0x3D010102), которое включает значение **emsabpUID**. Это значение **emsabpUID** определяет поставщика адресной книги Exchange для конкретного получателя.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="f89ea-150">Если вам нужно определить значение **emsabpUID** для идентификатора **emsmdbUID**, откройте раздел профиля для **emsmdbUID** и получите свойство **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="f89ea-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="f89ea-p112">Если вы вызываете метод [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), убедитесь, что получатели Exchange в передаваемом списке содержат свойство **PR_AB_PROVIDERS** с идентификатором **emsabpUID**, соответствующим поставщику адресной книги, к которому относится получатель. Вызов метода [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) для строки, полученной из метода [IAddrBook::ResolveName](iaddrbook-resolvename.md), не требует дополнительных действий, но некоторые фрагменты кода будет вызывать метод [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) для строк, содержащих только свойство **PR_ENTRYID**. В этой и других подобных ситуациях строки должны содержать свойства **PR_ENTRYID** и **PR_AB_PROVIDERS** со свойством **PR_AB_PROVIDERS**, где задан правильный идентификатор **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="f89ea-154">Ниже представлено простое описание процесса разрешения нескольких учетных записей Exchange.</span><span class="sxs-lookup"><span data-stu-id="f89ea-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="f89ea-p113">Получив уникальный идентификатор службы, код ищет таблицу хранилища сообщений, соответствующую свойству **PR_SERVICE_UID**, совпадающему с вашим. После этого вы можете определить правильное свойство **PR_MDB_PROVIDER**. В этой строке указывается соответствующее хранилище.</span><span class="sxs-lookup"><span data-stu-id="f89ea-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="f89ea-158">Получив **emsmdbUID**, код ищет в таблице служб сообщений строку, предоставляющую идентификатор **PidTagExchangeProfileSectionId**, который совпадает с **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f89ea-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f89ea-159">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f89ea-159">See also</span></span>



[<span data-ttu-id="f89ea-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="f89ea-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="f89ea-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="f89ea-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="f89ea-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="f89ea-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f89ea-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="f89ea-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f89ea-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="f89ea-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="f89ea-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="f89ea-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="f89ea-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="f89ea-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f89ea-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="f89ea-170">Каноническое свойство PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="f89ea-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="f89ea-171">Как открыть раздел глобального профиля</span><span class="sxs-lookup"><span data-stu-id="f89ea-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

