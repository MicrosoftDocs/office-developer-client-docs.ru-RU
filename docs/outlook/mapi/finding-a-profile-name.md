---
title: Поиск имени профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407923"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="8ef2e-103">Поиск имени профиля</span><span class="sxs-lookup"><span data-stu-id="8ef2e-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="8ef2e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ef2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ef2e-105">Иногда клиентам необходимо найти имя профиля, используемого в данный момент для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="8ef2e-106">Существует несколько способов получения имени профиля в ходе сеанса.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="8ef2e-107">Если необходимо найти имя профиля, которое необязательно является именем, используемым для сеанса, используйте первую процедуру.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="8ef2e-108">Чтобы найти имя профиля по умолчанию, используйте вторую процедуру.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="8ef2e-109">Если необходимо найти имя текущего профиля для сеанса, используйте последнюю процедуру.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="8ef2e-110">**Поиск имени любого профиля**</span><span class="sxs-lookup"><span data-stu-id="8ef2e-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="8ef2e-111">Вызовите [MAPIAdminProfiles,](mapiadminprofiles.md) чтобы получить указатель интерфейса **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="8ef2e-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="8ef2e-112">Вызовите [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="8ef2e-113">Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы профилей, чтобы получить все строки в таблице и проверить каждую из них, чтобы определить, представляет ли он целевой профиль.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="8ef2e-114">**Поиск имени профиля по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="8ef2e-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="8ef2e-115">Вызовите [MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="8ef2e-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="8ef2e-116">Вызовите [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="8ef2e-117">Создайте ограничение свойства со структурой [SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md)со значением TRUE.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="8ef2e-118">Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку в таблице профилей, которая представляет профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="8ef2e-119">Столбец **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)содержит имя профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="8ef2e-120">**Поиск имени текущего профиля**</span><span class="sxs-lookup"><span data-stu-id="8ef2e-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="8ef2e-121">Чтобы найти имя текущего профиля, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="8ef2e-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="8ef2e-122">Предположим, что у вас есть структура [MAPIUID,](mapiuid.md) представляющая один из разделов текущего профиля, передав его в _параметре lpUID_ [в IMAPISession::OpenProfileSection.](imapisession-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="8ef2e-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="8ef2e-123">Получите свойство PR_PROFILE_NAME раздела **профиля** [(PidTagProfileName)](pidtagprofilename-canonical-property.md)с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="8ef2e-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="8ef2e-124">Вызовите [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния и найти строку, для столбца **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)установлено значение MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="8ef2e-125">Столбец **PR_DISPLAY_NAME** для этой строки — это имя профиля.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="8ef2e-126">Не используйте таблицу состояния во время запуска, так как она блокирует приложение, пока пул mapI не завершит инициализацию всех поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="8ef2e-127">Это может ухудшить производительность.</span><span class="sxs-lookup"><span data-stu-id="8ef2e-127">This can degrade your performance.</span></span> 
    

