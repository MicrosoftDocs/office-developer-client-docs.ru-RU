---
title: Проверка конфигурации службы поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589639"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="ebf10-103">Проверка конфигурации службы поставщика</span><span class="sxs-lookup"><span data-stu-id="ebf10-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="ebf10-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebf10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebf10-105">Метод входа в систему ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) необходимо проверить конфигурацию вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="ebf10-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="ebf10-106">Это включает в себя проверки, что все свойства, необходимые для полного операции установлены правильно.</span><span class="sxs-lookup"><span data-stu-id="ebf10-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="ebf10-107">Каждый поставщик требуются разные число свойств; Конфигурация зависит от поставщика и степень взаимодействия с пользователем, то.</span><span class="sxs-lookup"><span data-stu-id="ebf10-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="ebf10-108">Некоторые поставщики услуг хранить все необходимые свойства в профиле.</span><span class="sxs-lookup"><span data-stu-id="ebf10-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="ebf10-109">Других поставщиков услуг, оставьте сокращенный набор свойств в профиле и запрашивать у пользователя для отсутствующие значения.</span><span class="sxs-lookup"><span data-stu-id="ebf10-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="ebf10-110">По-прежнему других поставщиков не следует хранить свойства профиля, от пользователя ввести все сведения, необходимые для настройки.</span><span class="sxs-lookup"><span data-stu-id="ebf10-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="ebf10-111">Для извлечения свойств, хранящиеся в профиле</span><span class="sxs-lookup"><span data-stu-id="ebf10-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="ebf10-112">Вызовите [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), передав [MAPIUID](mapiuid.md) поставщика в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="ebf10-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="ebf10-113">Вызов раздела профиля [IMAPIProp::GetProps](imapiprop-getprops.md) или [IMAPIProp::GetPropList](imapiprop-getproplist.md) методы для получения отдельных свойств или список свойств.</span><span class="sxs-lookup"><span data-stu-id="ebf10-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="ebf10-114">Для настройки свойств из сведений о пользователе</span><span class="sxs-lookup"><span data-stu-id="ebf10-114">To set properties from user information</span></span>
  
<span data-ttu-id="ebf10-115">Показывать на листе свойств MAPI не установлен флаг Запрет отображения.</span><span class="sxs-lookup"><span data-stu-id="ebf10-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="ebf10-116">Следующие флаги указывают, что пользовательский интерфейс не могут быть представлены.</span><span class="sxs-lookup"><span data-stu-id="ebf10-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="ebf10-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ebf10-117">**Flag**</span></span>|<span data-ttu-id="ebf10-118">**Поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="ebf10-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ebf10-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ebf10-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="ebf10-120">Поставщик адресной книги</span><span class="sxs-lookup"><span data-stu-id="ebf10-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="ebf10-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ebf10-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="ebf10-122">Поставщик транспорта</span><span class="sxs-lookup"><span data-stu-id="ebf10-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="ebf10-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ebf10-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="ebf10-124">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="ebf10-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="ebf10-125">Если ваш поставщик не сохраняет все его свойства конфигурации в профиле, требующее вмешательства пользователя и MAPI передает один из флагов блокировки отображения диалогового окна поле метод входа в систему, возвратите MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="ebf10-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="ebf10-126">Также возвратите Эта ошибка при флаг блокировки отображения диалогового окна не установлен, но пользователь не поддерживает все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="ebf10-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="ebf10-127">При сбое метода входа в систему с MAPI_E_UNCONFIGURED ваш поставщик услуг MAPI еще раз вызывает функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="ebf10-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="ebf10-128">Если сведения не удается найти на второй вызов, сеанс может завершить работу, в зависимости от того, насколько важна поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="ebf10-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="ebf10-129">На следующем рисунке показана логика, необходимые для настройки в методе службы поставщика входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ebf10-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="ebf10-130">**Блок-схема проверки конфигурации**</span><span class="sxs-lookup"><span data-stu-id="ebf10-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="ebf10-131">![Блок-схема проверки конфигурации] (media/amapi_62.gif "Блок-схема проверки конфигурации")</span><span class="sxs-lookup"><span data-stu-id="ebf10-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebf10-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ebf10-132">See also</span></span>

- [<span data-ttu-id="ebf10-133">Реализация входа для поставщика службы</span><span class="sxs-lookup"><span data-stu-id="ebf10-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

