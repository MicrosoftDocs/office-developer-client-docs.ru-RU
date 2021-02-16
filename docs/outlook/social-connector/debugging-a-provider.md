---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Существует несколько способов отлаки поставщика Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281071"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="5b228-103">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="5b228-103">Debugging a provider</span></span>

<span data-ttu-id="5b228-104">Существует несколько способов отлаки поставщика Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="5b228-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="5b228-105">Использование команд отлаки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или поддерживающих клиентские приложения Office приведет к тому, что osC будет принимать различные действия.</span><span class="sxs-lookup"><span data-stu-id="5b228-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="5b228-106">Использование Fiddler для отслеживания вызовов API и XML, отправленных между социальной сетью и ее поставщиком OSC</span><span class="sxs-lookup"><span data-stu-id="5b228-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="5b228-107">Кнопки отлаки</span><span class="sxs-lookup"><span data-stu-id="5b228-107">Debug buttons</span></span>

<span data-ttu-id="5b228-108">Возможность расшифровки поставщика OSC предоставляет возможность отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="5b228-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="5b228-109">Чтобы отладить поставщика, создайте значение типа DWORD в реестре Windows под ключом (как показано в следующей строке) и задайте значение  `DebugProviders`  `SocialConnector`  `DebugProviders` 1.</span><span class="sxs-lookup"><span data-stu-id="5b228-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="5b228-110">По умолчанию отладка поставщика отключена.</span><span class="sxs-lookup"><span data-stu-id="5b228-110">By default, provider debugging is off.</span></span> <span data-ttu-id="5b228-111">Если значение не присутствует или имеет значение 0, отладка поставщика  `DebugProviders` отключена.</span><span class="sxs-lookup"><span data-stu-id="5b228-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="5b228-112">Если отладка поставщика включена, OSC отображает диалоговое окно оповещения с подробными сведениями об ошибке при ошибке и проверяет любой XML-адрес поставщика OSC на XML-схеме поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="5b228-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="5b228-113">На основе пространства имен, указанного для строки XML, поставщик OSC, разработанный с помощью OSC 1.0, проверяется на основе файла схемы OSC 1.0 OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="5b228-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="5b228-114">Поставщик OSC, разработанный с помощью OSC 1.1 или более поздней, проверяется с использованием файла схемы, OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="5b228-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="5b228-115">При использовании значения оповещение отлажено для всех загруженных поставщиков, а не  `DebugProviders` для определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="5b228-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="5b228-116">Чтобы отобразить кнопки отлаки, которые помогут отлажать поставщика, создайте значение типа DWORD в реестре Windows под ключом и задайте значение  `ShowDebugButtons`  `SocialConnector`  `ShowDebugButtons` 1.</span><span class="sxs-lookup"><span data-stu-id="5b228-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="5b228-117">Чтобы скрыть кнопки панели команд отлаки, установите значение  `ShowDebugButtons` 0.</span><span class="sxs-lookup"><span data-stu-id="5b228-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="5b228-118">В Outlook 2010 и клиентских приложениях, начиная с Office 2013, кнопки отлаки отображаются на вкладке "Надстройки" ленты проводника. </span><span class="sxs-lookup"><span data-stu-id="5b228-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="5b228-119">В Outlook 2007 и Outlook 2003 кнопки отлаки отображаются на стандартной панели команд окна проводника Outlook.</span><span class="sxs-lookup"><span data-stu-id="5b228-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="5b228-120">В следующей таблице описаны кнопки отлаки.</span><span class="sxs-lookup"><span data-stu-id="5b228-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="5b228-121">**Кнопка отлаки**</span><span class="sxs-lookup"><span data-stu-id="5b228-121">**Debug button**</span></span>|<span data-ttu-id="5b228-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="5b228-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b228-123">Синхронизация контактов</span><span class="sxs-lookup"><span data-stu-id="5b228-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="5b228-124">Заставляет OSC запросить у поставщика OSC только кэшировать контакты.</span><span class="sxs-lookup"><span data-stu-id="5b228-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="5b228-125">Синхронизация gal</span><span class="sxs-lookup"><span data-stu-id="5b228-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="5b228-126">Вызывает заполнение osc данными из глобального списка адресов Exchange для контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="5b228-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="5b228-127">Недействительный кэш категорий</span><span class="sxs-lookup"><span data-stu-id="5b228-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="5b228-128">Вызывает перезагрузку списка категорий для каждого магазина при обновлении веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="5b228-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="5b228-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="5b228-129">Fiddler</span></span>

<span data-ttu-id="5b228-130">Fiddler — это средство отладки по сети для проверки вызовов API, отправленных поставщиком в социальные сети, и XML- и XML-данных, отправленных социальной сетью поставщику.</span><span class="sxs-lookup"><span data-stu-id="5b228-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="5b228-131">Fiddler можно скачать на [прокси-сервере веб-отладки Fiddler.](https://www.fiddler2.com/fiddler2/version.asp)</span><span class="sxs-lookup"><span data-stu-id="5b228-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b228-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5b228-132">See also</span></span>

- [<span data-ttu-id="5b228-133">Быстрые шаги по обучению разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="5b228-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="5b228-134">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="5b228-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="5b228-135">Best Practices for Developing a Provider</span><span class="sxs-lookup"><span data-stu-id="5b228-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="5b228-136">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="5b228-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="5b228-137">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="5b228-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="5b228-138">Getting Ready to Release an OSC Provider</span><span class="sxs-lookup"><span data-stu-id="5b228-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

