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
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="2e9c5-103">Проверка конфигурации поставщика службы</span><span class="sxs-lookup"><span data-stu-id="2e9c5-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="2e9c5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e9c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e9c5-105">Ваш метод logon[(IABProvider:::Logon,](iabprovider-logon.md) [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon)](ixpprovider-transportlogon.md)должен проверить конфигурацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="2e9c5-106">Это включает проверку правильности всех свойств, необходимых для полной работы.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="2e9c5-107">Каждому поставщику требуется различное количество свойств; конфигурация зависит от поставщика и степени взаимодействия с пользователем, который вы разрешаете.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="2e9c5-108">Некоторые поставщики услуг держат все необходимые свойства в профиле.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="2e9c5-109">Другие поставщики услуг держат частичный набор свойств в профиле и подсказывая пользователю отсутствующие значения.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="2e9c5-110">Однако другие поставщики вообще не хранят свойства в профиле, полагаясь на то, что пользователь должен предоставить всю необходимую информацию для настройки.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="2e9c5-111">Извлечение свойств, хранимых в профиле</span><span class="sxs-lookup"><span data-stu-id="2e9c5-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="2e9c5-112">Вызов [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md)передавая [MAPIUID](mapiuid.md) поставщика в качестве параметра ввода.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="2e9c5-113">Вызовите методы [IMAPIProp::GetProps](imapiprop-getprops.md) или [IMAPIProp::GetPropList](imapiprop-getproplist.md) для получения отдельных свойств или списка свойств.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="2e9c5-114">Настройка свойств из пользовательских сведений</span><span class="sxs-lookup"><span data-stu-id="2e9c5-114">To set properties from user information</span></span>
  
<span data-ttu-id="2e9c5-115">Отображение листа свойств, если MAPI не установил флаг, запрещающий отображение.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="2e9c5-116">Следующие флаги указывают, что пользовательский интерфейс не может быть представлен.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="2e9c5-117">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="2e9c5-117">**Flag**</span></span>|<span data-ttu-id="2e9c5-118">**Поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="2e9c5-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e9c5-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2e9c5-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="2e9c5-120">Поставщик адресных книг</span><span class="sxs-lookup"><span data-stu-id="2e9c5-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="2e9c5-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2e9c5-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="2e9c5-122">Поставщик транспорта</span><span class="sxs-lookup"><span data-stu-id="2e9c5-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="2e9c5-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2e9c5-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="2e9c5-124">Поставщик магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="2e9c5-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="2e9c5-125">Если поставщик не хранит все свои свойства конфигурации в профиле, требуя взаимодействия с пользователем, и MAPI передает один из флагов подавления диалоговых полей в метод logon, верните MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="2e9c5-126">Также возвращайте эту ошибку, когда флаг подавления диалогов не установлен, но пользователь не сообщает всю необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="2e9c5-127">Если поставщик услуг не работает с помощью метода MAPI_E_UNCONFIGURED, MAPI снова вызывает функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="2e9c5-128">Если данные не могут быть расположены при втором вызове, сеанс может завершиться в зависимости от того, насколько важен поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="2e9c5-129">На следующем рисунке показана логика, необходимая для настройки в методе logon поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2e9c5-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="2e9c5-130">**Блок-схема проверки конфигурации**</span><span class="sxs-lookup"><span data-stu-id="2e9c5-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="2e9c5-131">![Поток проверки конфигурации проверки](media/amapi_62.gif "конфигурации")</span><span class="sxs-lookup"><span data-stu-id="2e9c5-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e9c5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2e9c5-132">See also</span></span>

- [<span data-ttu-id="2e9c5-133">Реализация logon поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="2e9c5-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

