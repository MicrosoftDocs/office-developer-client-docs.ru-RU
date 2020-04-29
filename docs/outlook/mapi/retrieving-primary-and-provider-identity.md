---
title: Получение основного удостоверения и удостоверения поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430814"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="8078e-103">Получение основного удостоверения и удостоверения поставщика</span><span class="sxs-lookup"><span data-stu-id="8078e-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="8078e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8078e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8078e-105">Поставщики услуг, обычно поставщики адресных книг, предоставляют возможность указать идентификатор, который можно использовать для представления сеанса в различных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="8078e-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="8078e-106">Идентификатор поставщика описывается в трех свойствах:</span><span class="sxs-lookup"><span data-stu-id="8078e-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="8078e-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8078e-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="8078e-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8078e-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="8078e-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8078e-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="8078e-110">Эти свойства задаются как идентификатор записи, отображаемое имя и ключ поиска соответствующего объекта Identity, который обычно является пользователем системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8078e-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="8078e-111">Поставщики, которые предоставляют удостоверение, также устанавливают флаг STATUS_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8078e-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="8078e-112">В зависимости от ваших потребностей вы можете использовать идентификатор определенного поставщика или основной идентификатор сеанса.</span><span class="sxs-lookup"><span data-stu-id="8078e-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="8078e-113">Вы также можете использовать удостоверение поставщика для отображения или получения свойств, таких как **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8078e-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="8078e-114">**PR_RESOURCE_PATH**, если этот параметр установлен, содержит путь к файлам, используемым или созданным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8078e-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="8078e-115">Получите свойство **PR_RESOURCE_PATH** поставщика, предоставляющее Основное удостоверение, когда требуется найти файлы, которые относятся к пользователю сеанса.</span><span class="sxs-lookup"><span data-stu-id="8078e-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="8078e-116">**Получение удостоверения определенного поставщика**</span><span class="sxs-lookup"><span data-stu-id="8078e-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="8078e-117">Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="8078e-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="8078e-118">Создание ограничения с использованием структуры [спропертирестриктион](spropertyrestriction.md) для сравнения столбца **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) с именем указанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="8078e-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="8078e-119">Вызов [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения строки поставщика.</span><span class="sxs-lookup"><span data-stu-id="8078e-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="8078e-120">Удостоверение поставщика будет храниться в столбце **PR_IDENTITY_ENTRYID** (если он существует).</span><span class="sxs-lookup"><span data-stu-id="8078e-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="8078e-121">**Извлечение основного удостоверения для сеанса**</span><span class="sxs-lookup"><span data-stu-id="8078e-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="8078e-122">Call [IMAPISession:: куеридентити](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="8078e-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="8078e-123">**Куеридентити** базовые удостоверения сеанса для существования значения STATUS_PRIMARY_IDENTITY в столбце **PR_RESOURCE_FLAGS** для одной из строк в таблице Status.</span><span class="sxs-lookup"><span data-stu-id="8078e-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="8078e-124">Если ни для одной из строк состояния не задано это значение, **куеридентити** назначает идентификатор первому поставщику услуг, который задает три свойства PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="8078e-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="8078e-125">Если поставщик услуг не предоставляет удостоверение, **куеридентити** возвращает MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="8078e-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="8078e-126">В этом случае необходимо создать строку символов для представления универсального пользователя, который может служить в качестве основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="8078e-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="8078e-127">**Явное задание основного удостоверения для сеанса**</span><span class="sxs-lookup"><span data-stu-id="8078e-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="8078e-128">Call [имсгсервицеадмин:: сетпримаридентити](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="8078e-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="8078e-129">Передайте **мапиуид** для целевого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8078e-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

