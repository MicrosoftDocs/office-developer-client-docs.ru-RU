---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Схема XML Outlook поставщика социальных соединителем (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539257"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="ecb0a-103">Разработка поставщика с использованием схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="ecb0a-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="ecb0a-104">Схема XML Outlook поставщика социальных соединителем (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="ecb0a-105">Схема XML позволяет поставщику OSC указывать возможности поставщика, друзей и элементов каналов активности в социальной сети с помощью трех основных элементов, **возможностей,** друзей и элементов **activityFeed** и их детских элементов.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="ecb0a-106">Поставщик OSC реализует интерфейсы и их методы в extensibility поставщика OSC, возвращая строки XML в качестве выходных параметров, которые соответствуют схеме XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="ecb0a-107">OsC вызывает эти методы для получения информации, которую она может понять, как определено схемой XML.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ecb0a-108">Экстенсивность поставщика OSC поддерживает отладку поставщиков, устанавливая значение ключа реестра `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` до 1.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="ecb0a-109">При включении отладки поставщика OSC проверяет XML поставщика на версию схемы XML OSC, указанную в атрибуте **XML xmlns.**</span><span class="sxs-lookup"><span data-stu-id="ecb0a-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="ecb0a-110">Для OSC 1.1 и версий OSC с Outlook Social Connector 2013 укажите атрибут **xmlns** следующим образом:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="ecb0a-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ecb0a-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="ecb0a-111">In this section</span></span>

- <span data-ttu-id="ecb0a-112">[Синхронизация друзей](synchronizing-friends-and-activities.md)и действий. Описывает различные способы синхронизации друзей, не друзей и действий в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="ecb0a-113">[Примеры XML поставщика OSC:](osc-provider-xml-examples.md)Включает примеры XML, которые показывают, как указать возможности поставщика OSC, друзей и элементов каналов активности в социальной сети с помощью схемы XML OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="ecb0a-114">[XML для](xml-for-capabilities.md)возможностей. Объясняет метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) который OSC использует для получения сведений о возможностях, выраженных в возможностях **XML,** от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="ecb0a-115">В этом разделе также описываются элементы XML в схеме XML-поставщика OSC, которые позволяют поставщику OSC указать его функциональность, в том числе то, как он обеспечивает проверку подлинности пользователей и синхронизирует работу с друзьями и действиями.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="ecb0a-116">[XML для друзей.](xml-for-friends.md)Приводит примеры API, которые OSC использует для получения сведений друзей, выраженных в **друзьях** XML, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="ecb0a-117">В этом разделе также описываются элементы XML **друзей.**</span><span class="sxs-lookup"><span data-stu-id="ecb0a-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="ecb0a-118">[XML для действий](xml-for-activities.md). Приводит примеры API, которые OSC использует для получения сведений о действиях, выраженных в **activityFeed** XML, от поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="ecb0a-119">В этом разделе также описываются элементы XML в схеме XML поставщика OSC, которые позволяют поставщику OSC указывать канал активности.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="ecb0a-120">Канал действий включает сеть, в которой появились элементы ленты действий, сведения о каждом элементе ленты действий (например, владелец, тип и дата публикации действия), а также шаблон для отображения действия.</span><span class="sxs-lookup"><span data-stu-id="ecb0a-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="ecb0a-121">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="ecb0a-121">Reference</span></span>

- [<span data-ttu-id="ecb0a-122">Outlook Справка о поставщике социальных соединители</span><span class="sxs-lookup"><span data-stu-id="ecb0a-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ecb0a-123">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="ecb0a-123">Related sections</span></span>

- [<span data-ttu-id="ecb0a-124">Начало работы с разработкой Outlook поставщика социальных соединители</span><span class="sxs-lookup"><span data-stu-id="ecb0a-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="ecb0a-125">Шаблоны образцов OSC</span><span class="sxs-lookup"><span data-stu-id="ecb0a-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ecb0a-126">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="ecb0a-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="ecb0a-127">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="ecb0a-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ecb0a-128">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="ecb0a-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ecb0a-129">Лучшие практики для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="ecb0a-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ecb0a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ecb0a-130">See also</span></span>

- [<span data-ttu-id="ecb0a-131">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="ecb0a-131">Debugging a Provider</span></span>](debugging-a-provider.md)

