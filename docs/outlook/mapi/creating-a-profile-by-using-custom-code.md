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
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="a55c0-103">Создание профиля с помощью пользовательского кода</span><span class="sxs-lookup"><span data-stu-id="a55c0-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="a55c0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a55c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a55c0-105">Если вы решите написать код для создания профиля, убедитесь, что вы понимаете, как заказать записи профилей, а также тип и объем информации, необходимый для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="a55c0-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="a55c0-106">Последствия заказа записей в профиле объясняются в [профилях MAPI.](mapi-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a55c0-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="a55c0-107">**Создание профиля с кодом C или C++**</span><span class="sxs-lookup"><span data-stu-id="a55c0-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="a55c0-108">Ознакомьтесь с файлом загона для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a55c0-108">Read the header file for each message service.</span></span> <span data-ttu-id="a55c0-109">Поймите, какие свойства необходимо настроить и какие значения вы будете использовать.</span><span class="sxs-lookup"><span data-stu-id="a55c0-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="a55c0-110">Вызов [функции MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="a55c0-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="a55c0-111">Вызов [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="a55c0-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="a55c0-112">Если вы хотите создать профиль со службами сообщений, перечисленными в **разделе [Службы** по умолчанию] MAPISVC. Файл INF, установите флаг MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="a55c0-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="a55c0-113">Если вы хотите включить пользователю ввод сведений о конфигурации, установите флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="a55c0-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="a55c0-114">Убедитесь, что этот флаг установлен, если не вся необходимая информация доступна через MAPISVC. Файл INF.</span><span class="sxs-lookup"><span data-stu-id="a55c0-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="a55c0-115">**CreateProfile** вызывает функцию точки входа для каждой службы сообщений, которая будет добавлена в профиль с MSG_SERVICE_CREATE в качестве _параметра ulContext._</span><span class="sxs-lookup"><span data-stu-id="a55c0-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="a55c0-116">Вызов [IProfAdmin::AdminServices для](iprofadmin-adminservices.md) получения объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a55c0-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="a55c0-117">Используйте объект администрирования служб сообщений, чтобы добавить службы сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="a55c0-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="a55c0-118">Для каждой службы сообщений, которую необходимо добавить:</span><span class="sxs-lookup"><span data-stu-id="a55c0-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="a55c0-119">Вызов метода [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) для создания новой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a55c0-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="a55c0-120">Вызов [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md)передав структуру **MAPIUID** только что созданной службы и массив свойств со свойствами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a55c0-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="a55c0-121">Чтобы получить идентификатор недавно добавленной **службы,** которая является ее свойством [PR_SERVICE_UID (PidTagServiceUid),](pidtagserviceuid-canonical-property.md)позвоните [в службу IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений и поиска строки, представляющем службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="a55c0-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="a55c0-122">Последняя строка в таблице будет представлять последнюю добавленную службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="a55c0-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="a55c0-123">Чтобы сделать новый профиль временным, немедленно после входа вызывайте метод [IProfAdmin::D eleteProfile.](iprofadmin-deleteprofile.md)</span><span class="sxs-lookup"><span data-stu-id="a55c0-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="a55c0-124">**DeleteProfile** будет отмечать новый профиль как удаленный, делая его годным для работы в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="a55c0-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="a55c0-125">Так как она не будет включена в таблицу профилей сеанса, другие клиенты не смогут ее использовать.</span><span class="sxs-lookup"><span data-stu-id="a55c0-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

