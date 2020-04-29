---
title: Проверка конфигурации поставщика службы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418850"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="d54da-103">Проверка конфигурации поставщика службы</span><span class="sxs-lookup"><span data-stu-id="d54da-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="d54da-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d54da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d54da-105">Метод входа ([иабпровидер:: logon](iabprovider-logon.md), [Функцииimsprovider:: logon](imsprovider-logon.md)или [иксппровидер:: транспортлогон](ixpprovider-transportlogon.md)) должен проверить конфигурацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="d54da-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="d54da-106">Это включает проверку правильности настройки всех свойств, необходимых для полной операции.</span><span class="sxs-lookup"><span data-stu-id="d54da-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="d54da-107">Каждому поставщику необходимо различное количество свойств; Настройка зависит от поставщика и степени взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="d54da-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="d54da-108">Некоторые поставщики услуг хранят все необходимые свойства в профиле.</span><span class="sxs-lookup"><span data-stu-id="d54da-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="d54da-109">Другие поставщики услуг хранят частичный набор свойств в профиле и запрашивают у пользователя недостающие значения.</span><span class="sxs-lookup"><span data-stu-id="d54da-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="d54da-110">Другие поставщики по-прежнему не хранят свойства в профиле вообще, полагаться на то, что пользователь должен предоставить всю информацию, необходимую для настройки.</span><span class="sxs-lookup"><span data-stu-id="d54da-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="d54da-111">Извлечение свойств, хранящихся в профиле</span><span class="sxs-lookup"><span data-stu-id="d54da-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="d54da-112">Call [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md), передавая [мапиуид](mapiuid.md) поставщика в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="d54da-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="d54da-113">Вызовите методы [IMAPIProp::](imapiprop-getprops.md) GetProperty или [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , чтобы получить отдельные свойства или список свойств.</span><span class="sxs-lookup"><span data-stu-id="d54da-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="d54da-114">Задание свойств сведений о пользователе</span><span class="sxs-lookup"><span data-stu-id="d54da-114">To set properties from user information</span></span>
  
<span data-ttu-id="d54da-115">Отображение страницы свойств, если в MAPI не установлен флаг, запрещающий отображение.</span><span class="sxs-lookup"><span data-stu-id="d54da-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="d54da-116">Следующие флаги указывают на то, что пользовательский интерфейс не может быть представлен.</span><span class="sxs-lookup"><span data-stu-id="d54da-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="d54da-117">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="d54da-117">**Flag**</span></span>|<span data-ttu-id="d54da-118">**Поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="d54da-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d54da-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d54da-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="d54da-120">Поставщик адресных книг</span><span class="sxs-lookup"><span data-stu-id="d54da-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="d54da-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d54da-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="d54da-122">Поставщик транспорта</span><span class="sxs-lookup"><span data-stu-id="d54da-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="d54da-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d54da-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="d54da-124">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="d54da-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="d54da-125">Если поставщик не сохраняет все свойства конфигурации в профиле, требуя взаимодействия с пользователем, а MAPI передает один из флагов блокировки диалогового окна в метод входа, возвращается MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="d54da-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="d54da-126">Также возвращайте эту ошибку, если не установлен флаг запрета диалоговых окон, но пользователь не предоставляет все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="d54da-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="d54da-127">Если поставщик услуг не смог выполнить вход в систему с MAPI_E_UNCONFIGURED, MAPI повторно вызывает функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="d54da-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="d54da-128">Если не удается найти информацию при втором вызове, сеанс может завершиться в зависимости от того, насколько важен ваш поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="d54da-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="d54da-129">На следующем рисунке показана логика, необходимая для настройки в методе входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d54da-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="d54da-130">**Блок-схема проверки конфигурации**</span><span class="sxs-lookup"><span data-stu-id="d54da-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="d54da-131">![Configuration verification flowchart](media/amapi_62.gif "Блок-схема проверки конфигурации") блок-схемы проверки конфигурации</span><span class="sxs-lookup"><span data-stu-id="d54da-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d54da-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d54da-132">See also</span></span>

- [<span data-ttu-id="d54da-133">Реализация входа у поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="d54da-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

