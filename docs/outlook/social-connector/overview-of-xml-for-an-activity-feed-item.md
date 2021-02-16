---
title: Обзор XML для элемента веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Веб-канал активности состоит из одного или нескольких действий, происходящих в социальной сети. Каждый веб-канал активности представлен элементом activityFeed и характеризуется этими тремя элементами информации:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439949"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="252c4-104">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="252c4-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="252c4-105">Веб-канал активности состоит из одного или нескольких действий, происходящих в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="252c4-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="252c4-106">Каждый веб-канал активности представлен элементом **activityFeed** и характеризуется этими тремя элементами информации:</span><span class="sxs-lookup"><span data-stu-id="252c4-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="252c4-107">**сеть**— имя социальной сети, из которой были произведены действия.</span><span class="sxs-lookup"><span data-stu-id="252c4-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="252c4-108">**activities**— контейнер для действий, происходящих в учетной записи пользователя, выехав в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="252c4-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="252c4-109">**templates**— контейнер для шаблонов, используемых для отображения соответствующего элемента действия в **действиях.**</span><span class="sxs-lookup"><span data-stu-id="252c4-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="252c4-110">Чтобы создать элемент веб-канала активности, необходимо соответствовать XML-схеме extensibility поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="252c4-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="252c4-111">На рисунке 1 показана структура XML веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="252c4-112">**Рисунок 1. Структура XML веб-канала активности**</span><span class="sxs-lookup"><span data-stu-id="252c4-112">**Figure 1. Activity feed XML structure**</span></span>

![XML-структура новостей](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="252c4-114">Для каждого элемента веб-канала активности наиболее важными частями этой схемы являются элементы **activityDetails** и **activityTemplateContainer:**</span><span class="sxs-lookup"><span data-stu-id="252c4-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="252c4-115">В **элементе activityDetails** хранится определенная информация для каждого элемента веб-канала активности, например имя владельца действия или URL-адрес загруженных изображений.</span><span class="sxs-lookup"><span data-stu-id="252c4-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="252c4-116">Элемент **activityTemplateContainer** сохраняет формат или макет для каждого элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="252c4-117">Он состоит из шаблонов, представленных отдельными элементами **activityTemplate,** которые можно повторно использовать для нескольких элементов веб-канала.</span><span class="sxs-lookup"><span data-stu-id="252c4-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="252c4-118">Для отдельного элемента веб-канала активности элемент **activityTemplate** указывает следующие четыре элемента информации:</span><span class="sxs-lookup"><span data-stu-id="252c4-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="252c4-119">**icon**— указывает URL-адрес значка для отображения элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="252c4-120">**title**— описывает элемент веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="252c4-121">**type**— указывает тип действия, например состояние, фотографию или обновление документа.</span><span class="sxs-lookup"><span data-stu-id="252c4-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="252c4-122">**data**— указывает любую дополнительную информацию, отображаемую с помощью элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="252c4-123">Значок, отображаемой в веб-канале активности, всегда такой же, как и значок поставщика, возвращенный свойством **ISocialProvider::SocialNetworkIcon.**</span><span class="sxs-lookup"><span data-stu-id="252c4-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="252c4-124">Дополнительные сведения об элементе **activityDetails,** элементе **activityTemplateContainer,** маркерах шаблонов и переменных шаблона см. в следующих подразделах:</span><span class="sxs-lookup"><span data-stu-id="252c4-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="252c4-125">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="252c4-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="252c4-126">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="252c4-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="252c4-127">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="252c4-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="252c4-128">Руководство по правильному отобралку действий</span><span class="sxs-lookup"><span data-stu-id="252c4-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="252c4-129">Пример XML-канала активности см. в [XML-примере](activity-feed-xml-example.md)веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="252c4-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="252c4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="252c4-130">See also</span></span>

- [<span data-ttu-id="252c4-131">XML для действий</span><span class="sxs-lookup"><span data-stu-id="252c4-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="252c4-132">XML-схема поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="252c4-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="252c4-133">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="252c4-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

