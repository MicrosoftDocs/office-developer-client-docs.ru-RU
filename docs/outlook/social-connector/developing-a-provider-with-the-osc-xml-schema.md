---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539257"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="563e1-103">Разработка поставщика с использованием схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="563e1-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="563e1-104">XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.</span><span class="sxs-lookup"><span data-stu-id="563e1-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="563e1-105">Схема XML позволяет поставщику OSC указывать возможности поставщика, друзей и элементов веб-канала активности в социальной сети с помощью трех основных элементов, **возможностей,** друзей и **activityFeed** и их потомков.</span><span class="sxs-lookup"><span data-stu-id="563e1-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="563e1-106">Поставщик OSC реализует интерфейсы и их методы в реализации возможностей поставщика OSC, возвращая строки XML в качестве выходных параметров, которые соответствуют XML-схеме поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="563e1-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="563e1-107">OsC вызывает эти методы для получения сведений, которые могут быть понятны в схеме XML.</span><span class="sxs-lookup"><span data-stu-id="563e1-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="563e1-108">Возможность extensibility поставщика OSC поддерживает поставщиков отладки, устанавливая для ключа реестра значение `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 1.</span><span class="sxs-lookup"><span data-stu-id="563e1-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="563e1-109">При включении отладки поставщика OSC проверяет XML поставщика на основе версии схемы OSC XML, задаемой в атрибуте **XML xmlns.**</span><span class="sxs-lookup"><span data-stu-id="563e1-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="563e1-110">Для OSC 1.1 и версий OSC, начиная с Outlook Social Connector 2013, укажите **атрибут xmlns** следующим образом: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="563e1-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="563e1-111">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="563e1-111">In this section</span></span>

- <span data-ttu-id="563e1-112">[Синхронизация друзей](synchronizing-friends-and-activities.md)и действий : описание различных способов, которыми поставщики OSC могут синхронизировать друзей, не друзей и действия в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="563e1-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="563e1-113">[XML-примеры](osc-provider-xml-examples.md)поставщика OSC : содержит примеры XML, которые показывают, как задать возможности поставщика OSC, друзей и элементов веб-канала активности в социальной сети с помощью схемы OSC XML.</span><span class="sxs-lookup"><span data-stu-id="563e1-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="563e1-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span><span class="sxs-lookup"><span data-stu-id="563e1-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="563e1-115">В этом разделе также описываются XML-элементы схемы XML поставщика OSC, которые позволяют поставщику OSC указывать свои функции, включая проверку подлинности пользователей и синхронизацию друзей и действий.</span><span class="sxs-lookup"><span data-stu-id="563e1-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="563e1-116">[XML для друзей](xml-for-friends.md): предоставляет примеры API, которые OSC использует для получения сведений о друзьях, выраженных **в** XML друзей, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="563e1-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="563e1-117">В этом разделе также описываются элементы **XML-разных друзей.**</span><span class="sxs-lookup"><span data-stu-id="563e1-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="563e1-118">[XML для действий](xml-for-activities.md): предоставляет примеры API, которые OSC использует для получения сведений о действиях, выраженных в **XML activityFeed,** от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="563e1-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="563e1-119">В этом разделе также описываются XML-элементы в XML-схеме поставщика OSC, которые позволяют поставщику OSC указывать веб-канал активности.</span><span class="sxs-lookup"><span data-stu-id="563e1-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="563e1-120">Веб-канал активности включает сеть, в которой ились элементы веб-канала активности, сведения о каждом элементе веб-канала активности (например, владелец, тип и дата публикации действия) и шаблон для отображения действия.</span><span class="sxs-lookup"><span data-stu-id="563e1-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="563e1-121">Справка</span><span class="sxs-lookup"><span data-stu-id="563e1-121">Reference</span></span>

- [<span data-ttu-id="563e1-122">Outlook Social Connector Provider Reference</span><span class="sxs-lookup"><span data-stu-id="563e1-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="563e1-123">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="563e1-123">Related sections</span></span>

- [<span data-ttu-id="563e1-124">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="563e1-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="563e1-125">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="563e1-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="563e1-126">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="563e1-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="563e1-127">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="563e1-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="563e1-128">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="563e1-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="563e1-129">Best Practices for Developing a Provider</span><span class="sxs-lookup"><span data-stu-id="563e1-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="563e1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="563e1-130">See also</span></span>

- [<span data-ttu-id="563e1-131">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="563e1-131">Debugging a Provider</span></span>](debugging-a-provider.md)

