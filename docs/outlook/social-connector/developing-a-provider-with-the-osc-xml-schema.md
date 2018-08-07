---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительное сведения, передаваемые из социальных сетей через сеть OSC поставщика OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812723"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="bd838-103">Разработка поставщика с использованием схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="bd838-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="bd838-104">XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительное сведения, передаваемые из социальных сетей через сеть OSC поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="bd838-105">Схема XML позволяет поставщика OSC для указания возможностей поставщика, друзей и веб-канал элементов в социальных сетях, используя три основных элемента, **возможности**, **друзей**и **activityFeed**и их дочерних активности элементы.</span><span class="sxs-lookup"><span data-stu-id="bd838-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="bd838-106">Поставщика OSC реализует интерфейсы и методы их возможности расширения поставщика OSC возвращение строк XML как выходные параметры, совместимые с использованием схемы XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="bd838-107">OSC вызывает эти методы для получения информации, которая понять, как указано в схеме XML.</span><span class="sxs-lookup"><span data-stu-id="bd838-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bd838-108">Возможности расширения поставщика OSC поддерживает отладки поставщиков, задав `DebugProviders` значение `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` раздела реестра значение 1.</span><span class="sxs-lookup"><span data-stu-id="bd838-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="bd838-109">При включении отладки поставщика OSC проверяет поставщика XML для версии схемы XML для OSC, указанные в XML-атрибут **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="bd838-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="bd838-110">Для OSC 1.1 и версий OSC с момента Outlook Social Connector 2013 укажите атрибут **xmlns** следующим образом.`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="bd838-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bd838-111">В этой статье</span><span class="sxs-lookup"><span data-stu-id="bd838-111">In this section</span></span>

- <span data-ttu-id="bd838-112">[Синхронизация друзей и действий](synchronizing-friends-and-activities.md): описываются различные способы, поставщики OSC можно синхронизировать друзей, не являющиеся друзей и действий в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="bd838-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="bd838-113">[Примеры XML поставщика OSC](osc-provider-xml-examples.md): включает в себя XML примеры, показывающие, как для указания возможностей поставщика OSC, друзей и активности веб-канала элементы в социальных сетях с использованием схемы XML для OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="bd838-114">[XML-код для возможности](xml-for-capabilities.md): описание - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) метод, который OSC используется для получения сведений о возможностях, выраженная в **возможности** XML, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="bd838-115">В этом разделе также описываются элементы XML в XML-схему поставщика OSC, позволяющих поставщика OSC указать его функциональные возможности, включая как оно выполняет проверку подлинности пользователей, а также сведения об друзей и действия.</span><span class="sxs-lookup"><span data-stu-id="bd838-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="bd838-116">[XML-код для друзей](xml-for-friends.md): приведены примеры интерфейсов API, OSC для получения сведений о друзей, выраженная в **друзья** XML, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="bd838-117">В этом разделе также описываются элементы в **друзья** XML.</span><span class="sxs-lookup"><span data-stu-id="bd838-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="bd838-118">[XML-код для действий](xml-for-activities.md): приведены примеры интерфейсов API, OSC для получения сведений о действиях, выраженная в **activityFeed** XML, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="bd838-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="bd838-119">В этом разделе также описываются элементы XML в XML-схему поставщика OSC, позволяющих поставщика OSC указать веб-канал активности.</span><span class="sxs-lookup"><span data-stu-id="bd838-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="bd838-120">Веб-канал активности включает в себя сеть, где веб-канала активности элементов была создана, подробные сведения для каждого веб-канал активности элемента (например, владельца, введите и дата действия публикации) и шаблон для отображения действия.</span><span class="sxs-lookup"><span data-stu-id="bd838-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="bd838-121">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="bd838-121">Reference</span></span>

- [<span data-ttu-id="bd838-122">Справочник поставщика по Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="bd838-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="bd838-123">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="bd838-123">Related sections</span></span>

- [<span data-ttu-id="bd838-124">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="bd838-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="bd838-125">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="bd838-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="bd838-126">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="bd838-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="bd838-127">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="bd838-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="bd838-128">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="bd838-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="bd838-129">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="bd838-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="bd838-130">См. также</span><span class="sxs-lookup"><span data-stu-id="bd838-130">See also</span></span>

- [<span data-ttu-id="bd838-131">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="bd838-131">Debugging a Provider</span></span>](debugging-a-provider.md)

