---
title: Поиск имени профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808436"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="2c373-103">Поиск имени профиля</span><span class="sxs-lookup"><span data-stu-id="2c373-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="2c373-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c373-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c373-105">Клиенты в некоторых случаях требуется найти имя профиля, используемого сейчас для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленный на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2c373-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="2c373-106">Существует несколько способов получить имя профиля в ходе сеанса.</span><span class="sxs-lookup"><span data-stu-id="2c373-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="2c373-107">Чтобы найти имя профиля, который не обязательно, используемый для сеанса, используйте первой процедуры.</span><span class="sxs-lookup"><span data-stu-id="2c373-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="2c373-108">Если требуется найти имя профиля по умолчанию, используйте во второй процедуре.</span><span class="sxs-lookup"><span data-stu-id="2c373-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="2c373-109">Чтобы найти имя текущего профиля для сеанса, используйте последнего действия.</span><span class="sxs-lookup"><span data-stu-id="2c373-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="2c373-110">**Чтобы найти имя любого профиля**</span><span class="sxs-lookup"><span data-stu-id="2c373-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="2c373-111">Вызов [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="2c373-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="2c373-112">Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="2c373-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2c373-113">Вызов метода [IMAPITable::QueryRows](imapitable-queryrows.md) в таблице профиля для извлечения все строки в таблице и проверить каждый из них для определения, если он представляет своего профиля целевой.</span><span class="sxs-lookup"><span data-stu-id="2c373-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="2c373-114">**Чтобы найти имя профиля по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="2c373-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="2c373-115">Вызов [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="2c373-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="2c373-116">Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="2c373-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2c373-117">Выполните построение ограничение свойства с [SPropertyRestriction](spropertyrestriction.md) структурой в соответствии со значением TRUE **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c373-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="2c373-118">Вызов [IMAPITable::FindRow](imapitable-findrow.md) найдите строку в таблице профиля, который представляет профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c373-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="2c373-119">В столбце **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) содержит имя профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c373-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="2c373-120">**Чтобы найти имя текущего профиля**</span><span class="sxs-lookup"><span data-stu-id="2c373-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="2c373-121">Чтобы найти имя текущего профиля, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="2c373-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="2c373-122">Если предполагается, что у вас есть структура [MAPIUID](mapiuid.md) , представляющий один из разделов текущего профиля, передайте в него с помощью параметра _lpUID_ [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="2c373-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="2c373-123">Получение свойства **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) в разделе профилей с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="2c373-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="2c373-124">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния и найдите строку, задайте значение MAPI_SUBSYSTEM столбец **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c373-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="2c373-125">В столбце **PR_DISPLAY_NAME** для этой строки — имя профиля.</span><span class="sxs-lookup"><span data-stu-id="2c373-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="2c373-126">Не используйте в таблице состояния во время начала из-за его блокирует приложения до завершения инициализации всех поставщиков транспорта диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c373-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="2c373-127">Это может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="2c373-127">This can degrade your performance.</span></span> 
    

