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
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="07b8a-103">Создание профиля с помощью пользовательского кода</span><span class="sxs-lookup"><span data-stu-id="07b8a-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="07b8a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07b8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07b8a-105">Если вы напишете код для создания профиля, убедитесь, что вы знаете, как упорядочивать записи профиля, а также тип и количество сведений, необходимых для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="07b8a-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="07b8a-106">Влияние порядка записей в профиле объясняется в профилях [MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="07b8a-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="07b8a-107">**Создание профиля с кодом C или C++**</span><span class="sxs-lookup"><span data-stu-id="07b8a-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="07b8a-108">ПроЧтите файл заголовка для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-108">Read the header file for each message service.</span></span> <span data-ttu-id="07b8a-109">Сведения о свойствах, которые необходимо настроить, и значениях, которые будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="07b8a-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="07b8a-110">ВыЗовите функцию [мапиадминпрофилес](mapiadminprofiles.md) , чтобы получить указатель интерфейса **ипрофадмин** .</span><span class="sxs-lookup"><span data-stu-id="07b8a-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="07b8a-111">Call [ипрофадмин:: креатепрофиле](iprofadmin-createprofile.md) для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="07b8a-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="07b8a-112">Если вы хотите создать профиль с помощью служб сообщений, перечисленных в разделе **[службы по умолчанию]** элемента Mapisvc. INF-файл, установите флаг МАПИ_ДЕФАУЛТ_СЕРВИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="07b8a-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="07b8a-113">Если вы хотите разрешить пользователю вводить сведения о конфигурации, установите флаг МАПИ_ДИАЛОГ.</span><span class="sxs-lookup"><span data-stu-id="07b8a-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="07b8a-114">Убедитесь, что установлен этот флаг, если не все необходимые сведения доступны через MAPISVC. INF-файл.</span><span class="sxs-lookup"><span data-stu-id="07b8a-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="07b8a-115">**Креатепрофиле** вызывает функцию точки входа для каждой службы сообщений, которую необходимо добавить в профиль с мсг_сервице_креате, установленным в качестве параметра _улконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="07b8a-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="07b8a-116">Call [ипрофадмин:: админсервицес](iprofadmin-adminservices.md) для получения объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="07b8a-117">Добавьте службы сообщений в профиль с помощью объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="07b8a-118">Для каждой службы сообщений, которую необходимо добавить:</span><span class="sxs-lookup"><span data-stu-id="07b8a-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="07b8a-119">ВыЗовите метод [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) , чтобы создать новую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="07b8a-120">Call [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md), передача структуры **мапиуид** только что созданной службы и массива значений свойств с его свойствами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="07b8a-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="07b8a-121">Чтобы получить идентификатор недавно добавленной службы, которая является свойством **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), вызовите [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) для доступа к таблице службы сообщений и поиска строки, представляющей Служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="07b8a-122">Последняя строка в таблице будет представлять недавно добавленную службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="07b8a-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="07b8a-123">Чтобы создать временный профиль, вызовите метод [ипрофадмин::D елетепрофиле](iprofadmin-deleteprofile.md) сразу после входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07b8a-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="07b8a-124">**Делетепрофиле** будет помечать новый профиль как удаленный, пока он будет использоваться в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="07b8a-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="07b8a-125">Так как он не будет включен в таблицу профилей сеанса, другие клиенты не смогут ее использовать.</span><span class="sxs-lookup"><span data-stu-id="07b8a-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

