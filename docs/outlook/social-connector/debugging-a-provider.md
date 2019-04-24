---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Существует несколько способов отладки поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281071"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="c5a8f-103">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="c5a8f-103">Debugging a provider</span></span>

<span data-ttu-id="c5a8f-104">Существует несколько способов отладки поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c5a8f-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="c5a8f-105">С помощью команд отладки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или поддерживающего клиентского приложения Office, чтобы OSC переводился на различные действия.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="c5a8f-106">С помощью Fiddler для трассировки вызовов API и XML-данных, передаваемых между социальной сетью и поставщиком OSC</span><span class="sxs-lookup"><span data-stu-id="c5a8f-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="c5a8f-107">Кнопки отладки</span><span class="sxs-lookup"><span data-stu-id="c5a8f-107">Debug buttons</span></span>

<span data-ttu-id="c5a8f-108">Расширяемость поставщика OSC предоставляет возможность отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="c5a8f-109">Чтобы выполнить отладку поставщика, создайте `DebugProviders` значение типа DWORD в реестре Windows в разделе `SocialConnector` Key (как показано в следующей строке) и присвойте этому `DebugProviders` параметру значение 1.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="c5a8f-110">По умолчанию Отладка поставщика отключена.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-110">By default, provider debugging is off.</span></span> <span data-ttu-id="c5a8f-111">Если `DebugProviders` значение отсутствует или присутствует, и для него задано значение 0, Отладка поставщика отключена.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="c5a8f-112">Если отладка поставщика включена, OSC отображает диалоговое окно оповещения с подробными сведениями об ошибке при возникновении ошибки и проверяет XML-код поставщика OSC на соответствие схеме XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="c5a8f-113">На основе пространства имен, указанного для строки XML, поставщик OSC, разработанный с помощью OSC 1,0, проверяется на соответствие файлу схемы OSC 1,0, АутлуксоЦиалпровидер. xsd.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="c5a8f-114">Поставщик OSC, разработанный с помощью OSC 1,1 или более поздней версии, проверяется на соответствие файлу схемы АутлуксоЦиалпровидер_ 1.1. xsd.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="c5a8f-115">При использовании `DebugProviders` значения предупреждение отладки отображается для всех загруженных поставщиков, а не для определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="c5a8f-116">Чтобы отобразить кнопки отладки, которые могут помочь при отладке поставщика, создайте `ShowDebugButtons` значение типа DWORD в реестре Windows в разделе `SocialConnector` Key и присвойте этому `ShowDebugButtons` параметру значение 1.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="c5a8f-117">Чтобы скрыть кнопки "Отладка" на панели команд `ShowDebugButtons` , установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="c5a8f-118">Для Outlook 2010 и клиентских приложений с момента выпуска Office 2013 кнопки отладки отображаются на вкладке \*\*\*\* "надстройки" ленты "Обозреватель".</span><span class="sxs-lookup"><span data-stu-id="c5a8f-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="c5a8f-119">Для Outlook 2007 и Outlook 2003 кнопки отладки отображаются на стандартной панели команд в окне проводника Outlook.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="c5a8f-120">В следующей таблице описываются кнопки отладки.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="c5a8f-121">**Кнопка "Отладка"**</span><span class="sxs-lookup"><span data-stu-id="c5a8f-121">**Debug button**</span></span>|<span data-ttu-id="c5a8f-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="c5a8f-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5a8f-123">Синхронизация контактов</span><span class="sxs-lookup"><span data-stu-id="c5a8f-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="c5a8f-124">Заставляет OSC запросить поставщика OSC только для кэшированных контактов.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="c5a8f-125">Синхронизация GAL</span><span class="sxs-lookup"><span data-stu-id="c5a8f-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="c5a8f-126">Заставляет OSC заполнить данные из глобального списка адресов Exchange в контакты Outlook.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="c5a8f-127">Непроверяемый кэш категорий</span><span class="sxs-lookup"><span data-stu-id="c5a8f-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="c5a8f-128">Заставляет OSC перезагружать список категорий для каждого хранилища при обновлении веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="c5a8f-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="c5a8f-129">Fiddler</span></span>

<span data-ttu-id="c5a8f-130">Fiddler — это средство отладки через сеть, которое проверяет вызовы API, отправленные поставщиком в социальную сеть, и XML-файл, отправленный социальной сетью поставщику.</span><span class="sxs-lookup"><span data-stu-id="c5a8f-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="c5a8f-131">Fiddler можно скачать на сайте [Fiddler Web Debugging proxy](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="c5a8f-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5a8f-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c5a8f-132">See also</span></span>

- [<span data-ttu-id="c5a8f-133">Быстрые действия для изучения разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="c5a8f-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="c5a8f-134">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="c5a8f-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="c5a8f-135">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="c5a8f-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="c5a8f-136">ПереOSC типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="c5a8f-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="c5a8f-137">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="c5a8f-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="c5a8f-138">Подготовка к выПуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="c5a8f-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

