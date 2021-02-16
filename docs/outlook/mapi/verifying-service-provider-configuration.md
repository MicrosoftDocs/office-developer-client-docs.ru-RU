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
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="179c9-103">Проверка конфигурации поставщика службы</span><span class="sxs-lookup"><span data-stu-id="179c9-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="179c9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="179c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="179c9-105">Метод для логотипа ([IABProvider::Logon,](iabprovider-logon.md) [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon)](ixpprovider-transportlogon.md)должен проверить конфигурацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="179c9-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="179c9-106">Это включает проверку правильности всех свойств, необходимых для полной работы.</span><span class="sxs-lookup"><span data-stu-id="179c9-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="179c9-107">Каждому поставщику требуется разное количество свойств; конфигурация зависит от поставщика и степени взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="179c9-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="179c9-108">Некоторые поставщики услуг сохраняют все необходимые свойства в профиле.</span><span class="sxs-lookup"><span data-stu-id="179c9-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="179c9-109">Другие поставщики услуг сохраняют частичный набор свойств в профиле и запросили у пользователя отсутствующие значения.</span><span class="sxs-lookup"><span data-stu-id="179c9-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="179c9-110">По-прежнему другие поставщики вообще не хранят свойства в профиле, полагаться на то, что пользователь должен предоставить всю информацию, необходимую для настройки.</span><span class="sxs-lookup"><span data-stu-id="179c9-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="179c9-111">Извлечение свойств, хранимых в профиле</span><span class="sxs-lookup"><span data-stu-id="179c9-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="179c9-112">Вызовите [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md)передав [MAPIUID](mapiuid.md) поставщика в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="179c9-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="179c9-113">Вызовите методы [IMAPIProp::GetProps](imapiprop-getprops.md) или [IMAPIProp::GetPropList](imapiprop-getproplist.md) раздела профиля, чтобы получить отдельные свойства или список свойств.</span><span class="sxs-lookup"><span data-stu-id="179c9-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="179c9-114">Настройка свойств из сведений о пользователе</span><span class="sxs-lookup"><span data-stu-id="179c9-114">To set properties from user information</span></span>
  
<span data-ttu-id="179c9-115">Отображение листа свойств, если MAPI не установил флаг, запрещающий отображение.</span><span class="sxs-lookup"><span data-stu-id="179c9-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="179c9-116">Следующие флаги указывают, что пользовательский интерфейс не может быть представлен.</span><span class="sxs-lookup"><span data-stu-id="179c9-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="179c9-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="179c9-117">**Flag**</span></span>|<span data-ttu-id="179c9-118">**Поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="179c9-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="179c9-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="179c9-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="179c9-120">Поставщик адресной книги</span><span class="sxs-lookup"><span data-stu-id="179c9-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="179c9-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="179c9-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="179c9-122">Поставщик транспорта</span><span class="sxs-lookup"><span data-stu-id="179c9-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="179c9-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="179c9-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="179c9-124">Поставщик store сообщений</span><span class="sxs-lookup"><span data-stu-id="179c9-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="179c9-125">Если поставщик не сохраняет все свойства конфигурации в профиле, требуя взаимодействия с пользователем, и MAPI передает один из флагов подавления диалоговых окна методу для MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="179c9-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="179c9-126">Также возвращает эту ошибку, если флаг подавления диалогов не установлен, но пользователь не сообщает всю необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="179c9-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="179c9-127">Если поставщик услуг не работает с методом входа с MAPI_E_UNCONFIGURED, MAPI снова вызывает функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="179c9-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="179c9-128">Если данные не могут быть расположены во втором вызове, сеанс может завершиться в зависимости от того, насколько важен поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="179c9-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="179c9-129">На следующем рисунке показана логика, необходимая для настройки в методе для работы с поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="179c9-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="179c9-130">**Блок-схема проверки конфигурации**</span><span class="sxs-lookup"><span data-stu-id="179c9-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="179c9-131">![Потоки проверки конфигурации](media/amapi_62.gif "конфигурации")</span><span class="sxs-lookup"><span data-stu-id="179c9-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="179c9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="179c9-132">See also</span></span>

- [<span data-ttu-id="179c9-133">Реализация службы для логоса</span><span class="sxs-lookup"><span data-stu-id="179c9-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

