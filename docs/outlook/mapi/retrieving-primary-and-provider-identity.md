---
title: Получение удостоверения поставщика и основного удостоверения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812143"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="bcf01-103">Получение удостоверения поставщика и основного удостоверения</span><span class="sxs-lookup"><span data-stu-id="bcf01-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="bcf01-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bcf01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bcf01-105">Поставщики услуг, обычно поставщиками адресных книг, имеют указать учетные данные, которые можно использовать для представления сеанса в различных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="bcf01-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="bcf01-106">Три свойства описывают поставщика удостоверений:</span><span class="sxs-lookup"><span data-stu-id="bcf01-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="bcf01-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bcf01-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="bcf01-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bcf01-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="bcf01-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bcf01-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="bcf01-110">Эти свойства устанавливаются идентификатор записи, отображаемое имя и ключ поиска соответствующего объекта удостоверения, как правило, обмена мгновенными сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="bcf01-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="bcf01-111">Поставщики, которые предоставить удостоверение также необходимо задать флаг STATUS_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bcf01-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bcf01-112">В зависимости от потребностей можно использовать определенного поставщика удостоверений или основной идентификатор для сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcf01-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="bcf01-113">Также для отображения или для извлечения свойств, таких как **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) можно использовать поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="bcf01-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="bcf01-114">**PR_RESOURCE_PATH**, если значение, содержащее пути к файлам, используемые или созданные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bcf01-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="bcf01-115">Извлечение свойства **PR_RESOURCE_PATH** для поставщика, передав основной идентификатор для поиска файлов, которые относятся к пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcf01-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="bcf01-116">**Чтобы получить идентификатор определенного поставщика**</span><span class="sxs-lookup"><span data-stu-id="bcf01-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="bcf01-117">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="bcf01-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="bcf01-118">Выполните построение ограничение с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с столбце **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) с именем указанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="bcf01-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="bcf01-119">Вызов [IMAPITable::FindRow](imapitable-findrow.md) найдите строку поставщика.</span><span class="sxs-lookup"><span data-stu-id="bcf01-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="bcf01-120">Поставщик удостоверений будет храниться в столбце **PR_IDENTITY_ENTRYID** , если он существует.</span><span class="sxs-lookup"><span data-stu-id="bcf01-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="bcf01-121">**Для извлечения основной идентификатор сеанса**</span><span class="sxs-lookup"><span data-stu-id="bcf01-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="bcf01-122">Вызов [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="bcf01-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="bcf01-123">**QueryIdentity** задает идентификатор сеанса на наличие STATUS_PRIMARY_IDENTITY значения в столбце **PR_RESOURCE_FLAGS** для одного из строки в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="bcf01-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="bcf01-124">Если ни одна из строки состояния значение, **QueryIdentity** назначает удостоверение первого поставщика услуг, который задает три свойства PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bcf01-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="bcf01-125">Если нет поставщик удостоверений, **QueryIdentity** возвращает MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="bcf01-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="bcf01-126">В этом случае необходимо создать строку знаков для представления универсальный пользователя, который может выступать в качестве основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="bcf01-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="bcf01-127">**Чтобы явно задать основной идентификатор сеанса**</span><span class="sxs-lookup"><span data-stu-id="bcf01-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="bcf01-128">Вызов [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="bcf01-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="bcf01-129">Передайте **MAPIUID** для поставщика услуг в целевой.</span><span class="sxs-lookup"><span data-stu-id="bcf01-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

