---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Существует несколько способов, чтобы выполнить отладку поставщика Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386854"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="77193-103">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="77193-103">Debugging a provider</span></span>

<span data-ttu-id="77193-104">Существует несколько способов, чтобы выполнить отладку поставщика Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="77193-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="77193-105">С помощью команды отладки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или вспомогательные клиентского приложения Office для OSC для выполнения различных действий.</span><span class="sxs-lookup"><span data-stu-id="77193-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="77193-106">С помощью Fiddler для трассировки API звонки и XML, передаваемая между социальной сети и его поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="77193-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="77193-107">Отладка кнопок</span><span class="sxs-lookup"><span data-stu-id="77193-107">Debug buttons</span></span>

<span data-ttu-id="77193-108">Возможности расширения поставщика OSC предоставляет возможность отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="77193-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="77193-109">Отладка поставщика, создайте `DebugProviders` значение введите значение DWORD в реестре Windows в разделе `SocialConnector` ключевые (как показано в следующей строке), а значение `DebugProviders` значение 1.</span><span class="sxs-lookup"><span data-stu-id="77193-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="77193-110">По умолчанию поставщик отладки отключен.</span><span class="sxs-lookup"><span data-stu-id="77193-110">By default, provider debugging is off.</span></span> <span data-ttu-id="77193-111">Если `DebugProviders` значение не задано, или присутствует и выключен присвоено значение 0, отладки поставщика.</span><span class="sxs-lookup"><span data-stu-id="77193-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="77193-112">Если включена отладка поставщика OSC отображает оповещения диалоговое окно со сведениями об ошибках verbose, когда ошибку и использует для проверки любого поставщика OSC XML соответствие схеме XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="77193-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="77193-113">Основываясь на пространство имен, указанное для XML-строка, поставщика OSC, разработанных с помощью OSC 1.0 проверяется файл схемы версии 1.0 OSC OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="77193-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="77193-114">Поставщика OSC разработанных с помощью OSC 1.1 или более поздней версии проверен файл схемы OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="77193-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="77193-115">При использовании `DebugProviders` значение, появляется уведомление о отладки для всех загруженных поставщиков вместо определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="77193-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="77193-116">Для отображения кнопки отладки, которые могут помочь в отладке поставщика, создайте `ShowDebugButtons` значение введите значение DWORD в реестре Windows в разделе `SocialConnector` ключа, а значение `ShowDebugButtons` значение 1.</span><span class="sxs-lookup"><span data-stu-id="77193-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="77193-117">Чтобы скрыть кнопки панели команд Отладка, задайте `ShowDebugButtons` значение 0.</span><span class="sxs-lookup"><span data-stu-id="77193-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="77193-118">Для Outlook 2010 и клиентских приложений с момента Office 2013 кнопки debug отображаются на вкладке **надстройки** на ленте explorer.</span><span class="sxs-lookup"><span data-stu-id="77193-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="77193-119">Для Outlook 2007 и Outlook 2003 кнопки debug отображаются на панели стандартных команд окно проводника Outlook.</span><span class="sxs-lookup"><span data-stu-id="77193-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="77193-120">В следующей таблице описываются кнопки отладки.</span><span class="sxs-lookup"><span data-stu-id="77193-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="77193-121">**Отладка кнопки**</span><span class="sxs-lookup"><span data-stu-id="77193-121">**Debug button**</span></span>|<span data-ttu-id="77193-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="77193-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77193-123">Синхронизация контактов</span><span class="sxs-lookup"><span data-stu-id="77193-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="77193-124">Вызывает OSC для запроса у поставщика OSC только кэшированные контакты.</span><span class="sxs-lookup"><span data-stu-id="77193-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="77193-125">Синхронизация глобального списка адресов</span><span class="sxs-lookup"><span data-stu-id="77193-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="77193-126">Вызывает OSC для заполнения данными из глобального списка адресов Exchange в список контактов.</span><span class="sxs-lookup"><span data-stu-id="77193-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="77193-127">Объявить недействительным кэш категории</span><span class="sxs-lookup"><span data-stu-id="77193-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="77193-128">Вызывает OSC будет перезагружена в список категорий для каждого хранилища при обновлении веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="77193-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="77193-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="77193-129">Fiddler</span></span>

<span data-ttu-id="77193-130">Fiddler — это средство отладки по сети для проверки вызовов API, отправленные от поставщика в социальной сети и XML, отправленные с социальной сети к поставщику.</span><span class="sxs-lookup"><span data-stu-id="77193-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="77193-131">Fiddler доступно для загрузки в [Fiddler отладки прокси-сервера](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="77193-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77193-132">См. также</span><span class="sxs-lookup"><span data-stu-id="77193-132">See also</span></span>

- [<span data-ttu-id="77193-133">Быстрый шаги, необходимые для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="77193-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="77193-134">Синхронизация друзей и действия</span><span class="sxs-lookup"><span data-stu-id="77193-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="77193-135">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="77193-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="77193-136">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="77193-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="77193-137">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="77193-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="77193-138">Подготовка к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="77193-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

