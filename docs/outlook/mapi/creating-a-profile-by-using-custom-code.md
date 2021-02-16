---
title: Создание профиля с помощью пользовательского кода
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413306"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="61a6b-103">Создание профиля с помощью пользовательского кода</span><span class="sxs-lookup"><span data-stu-id="61a6b-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="61a6b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61a6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61a6b-105">Если вы решили написать код для создания профиля, убедитесь, что вы понимаете, как заказать записи профиля, а также тип и объем информации, необходимый для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="61a6b-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="61a6b-106">Результаты упорядочения записей в профиле поясняется в [профилях MAPI.](mapi-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="61a6b-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="61a6b-107">**Создание профиля с кодом C или C++**</span><span class="sxs-lookup"><span data-stu-id="61a6b-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="61a6b-108">Прочитайте файл загона для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="61a6b-108">Read the header file for each message service.</span></span> <span data-ttu-id="61a6b-109">В этой теме поймут, какие свойства необходимо настроить и какие значения будут использовать.</span><span class="sxs-lookup"><span data-stu-id="61a6b-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="61a6b-110">Вызовите [функцию MAPIAdminProfiles,](mapiadminprofiles.md) чтобы получить указатель интерфейса **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="61a6b-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="61a6b-111">Вызовите [IProfAdmin::CreateProfile,](iprofadmin-createprofile.md) чтобы создать профиль.</span><span class="sxs-lookup"><span data-stu-id="61a6b-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="61a6b-112">Если вы хотите создать профиль со службами сообщений, перечисленными в разделе **[Службы** по умолчанию] MAPISVC. INF-файл, установите флаг MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="61a6b-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="61a6b-113">Если вы хотите включить для пользователя ввод сведений о конфигурации, установите MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="61a6b-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="61a6b-114">Убедитесь, что этот флаг установлен, если не все необходимые сведения доступны через MAPISVC. INF-файл.</span><span class="sxs-lookup"><span data-stu-id="61a6b-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="61a6b-115">**CreateProfile** вызывает функцию точки входа для каждой службы сообщений, добавляемой в профиль с MSG_SERVICE_CREATE в качестве параметра _ulContext._</span><span class="sxs-lookup"><span data-stu-id="61a6b-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="61a6b-116">Вызовите [IProfAdmin::AdminServices,](iprofadmin-adminservices.md) чтобы получить объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="61a6b-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="61a6b-117">Используйте объект администрирования службы сообщений для добавления служб сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="61a6b-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="61a6b-118">Для каждой службы сообщений, которую вы хотите добавить:</span><span class="sxs-lookup"><span data-stu-id="61a6b-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="61a6b-119">Вызовите [метод IMsgServiceAdmin::CreateMsgService,](imsgserviceadmin-createmsgservice.md) чтобы создать новую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="61a6b-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="61a6b-120">Вызовите [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md)передав структуру **MAPIUID** только что созданной службы и массив значений свойств со свойствами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61a6b-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="61a6b-121">Чтобы получить идентификатор только что добавленной службы, который является ее свойством **PR_SERVICE_UID** ([PidTagServiceUid),](pidtagserviceuid-canonical-property.md)вызовите [IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений и найти строку, которая представляет службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="61a6b-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="61a6b-122">Последняя строка в таблице представляет последнюю добавленную службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="61a6b-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="61a6b-123">Чтобы сделать новый профиль временным, вызовите метод [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) сразу после входа.</span><span class="sxs-lookup"><span data-stu-id="61a6b-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="61a6b-124">**DeleteProfile** пометит новый профиль как удаленный во время его работы в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="61a6b-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="61a6b-125">Так как она не будет включена в таблицу профилей сеанса, другие клиенты не смогут использовать ее.</span><span class="sxs-lookup"><span data-stu-id="61a6b-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

