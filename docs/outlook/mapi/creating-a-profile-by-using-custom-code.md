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
ms.openlocfilehash: 74869293215b86c69ab4e0b1337be6014419fa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808242"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="d411a-103">Создание профиля с помощью пользовательского кода</span><span class="sxs-lookup"><span data-stu-id="d411a-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="d411a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d411a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d411a-105">Если вы решаете написать код, чтобы создать профиль, убедитесь в том, что вам понять, как порядок записи профиля и тип и объем сведений, необходимых для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="d411a-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="d411a-106">Влияние на порядок записей в профиле объясняется [Профили MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="d411a-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="d411a-107">**Чтобы создать профиль с помощью кода C или C++**</span><span class="sxs-lookup"><span data-stu-id="d411a-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="d411a-108">Чтение файла заголовка для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d411a-108">Read the header file for each message service.</span></span> <span data-ttu-id="d411a-109">Понять, какие свойства, необходимо будет настроить и какие значения, которое будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="d411a-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="d411a-110">Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="d411a-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="d411a-111">Вызов [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="d411a-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="d411a-112">Если вы хотите создать профиль с помощью службы сообщений, перечисленных в разделе **[Службы по умолчанию]** файл Mapisvc.inf. INF-файл, задайте флаг MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="d411a-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="d411a-113">Чтобы разрешить пользователю требуется ввести сведения о конфигурации, установите флажок MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="d411a-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="d411a-114">Убедитесь в том, что установить этот флажок, если не все необходимые сведения, доступные через файл Mapisvc.inf. INF-файл.</span><span class="sxs-lookup"><span data-stu-id="d411a-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="d411a-115">**CreateProfile** вызывает функцию точки входа для каждой службы сообщения добавляется к профилю с MSG_SERVICE_CREATE установите в качестве параметра _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="d411a-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="d411a-116">Вызовите [IProfAdmin::AdminServices](iprofadmin-adminservices.md) , чтобы получить объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d411a-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="d411a-117">Используйте объект администрирования службы сообщений для добавления службы сообщений к профилю.</span><span class="sxs-lookup"><span data-stu-id="d411a-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="d411a-118">Для каждой службы сообщение, которое вы хотите добавить:</span><span class="sxs-lookup"><span data-stu-id="d411a-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="d411a-119">Вызовите метод [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) для создания новой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d411a-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="d411a-120">Вызовите [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), передав структура **MAPIUID** службу, которую вы только что создали и массива значение свойства с помощью его свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d411a-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="d411a-121">Для получения идентификатора новые службы, которая его свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), вызовите [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для доступа к таблице службы сообщений и поиск строку, представляющую Служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="d411a-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="d411a-122">Последняя строка в таблице будет представлять недавно добавлены службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d411a-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="d411a-123">Чтобы выбрать новый профиль временный, вызовите метод [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) сразу же после входа в систему.</span><span class="sxs-lookup"><span data-stu-id="d411a-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="d411a-124">**DeleteProfile** будут помечены новый профиль, как удаленное при выполнении можно использовать во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="d411a-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="d411a-125">Так как он не будет включаться в таблице профилей сеанса, других клиентов будет невозможно использовать его.</span><span class="sxs-lookup"><span data-stu-id="d411a-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

