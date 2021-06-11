---
title: Обзор XML для элемента веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Канал действий состоит из одной или нескольких действий, происходящих в социальной сети. Каждая лента действий представлена элементом activityFeed и характеризуется этими тремя частями информации:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439949"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="c3ebf-104">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="c3ebf-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="c3ebf-105">Канал действий состоит из одной или нескольких действий, происходящих в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="c3ebf-106">Каждая лента действий представлена элементом **activityFeed** и характеризуется этими тремя частями информации:</span><span class="sxs-lookup"><span data-stu-id="c3ebf-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="c3ebf-107">**network**—Name of the social network from which the activities originated.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="c3ebf-108">**действия**— контейнер для действий, происходящих в учетной записи пользователя в этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="c3ebf-109">**шаблоны**— контейнер для шаблонов, используемых для отображения соответствующего элемента активности в **действиях.**</span><span class="sxs-lookup"><span data-stu-id="c3ebf-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="c3ebf-110">Чтобы создать элемент ленты действий, необходимо соответствовать схеме XML Outlook поставщика Outlook (OSC).</span><span class="sxs-lookup"><span data-stu-id="c3ebf-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="c3ebf-111">На рисунке 1 показана структура XML-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="c3ebf-112">**Рис. 1. Структура XML-канала активности**</span><span class="sxs-lookup"><span data-stu-id="c3ebf-112">**Figure 1. Activity feed XML structure**</span></span>

![XML-структура новостей](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="c3ebf-114">Для каждого элемента ленты действий наиболее важными частями этой схемы являются элементы **activityDetails** и **activityTemplateContainer:**</span><span class="sxs-lookup"><span data-stu-id="c3ebf-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="c3ebf-115">Элемент **activityDetails** хранит определенные сведения для каждого элемента ленты действий, например имя владельца действия или URL-адрес для загруженных изображений.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="c3ebf-116">Элемент **activityTemplateContainer** сохраняет формат или макет для каждого элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="c3ebf-117">Он состоит из шаблонов, представленных отдельными элементами **activityTemplate,** которые можно повторно использовать для нескольких элементов питания.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="c3ebf-118">Для отдельного элемента ленты действий элемент **activityTemplate** указывает следующие четыре части информации:</span><span class="sxs-lookup"><span data-stu-id="c3ebf-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="c3ebf-119">**значок**— указывает URL-адрес для значка для отображения элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="c3ebf-120">**заголовок**—Описывает элемент ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="c3ebf-121">**тип**— указывает тип действий, таких как обновление состояния, фотографии или документа.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="c3ebf-122">**данные**— указывает любую дополнительную информацию, отображаемую с помощью элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="c3ebf-123">Значок, отображаемый в ленте действий, всегда такой же, как и значок поставщика, возвращенный свойством **ISocialProvider::SocialNetworkIcon.**</span><span class="sxs-lookup"><span data-stu-id="c3ebf-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="c3ebf-124">Дополнительные сведения о элементе **activityDetails,** **элементе activityTemplateContainer,** маркерах шаблонов и переменных шаблонов см. ниже.</span><span class="sxs-lookup"><span data-stu-id="c3ebf-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="c3ebf-125">элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="c3ebf-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="c3ebf-126">элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="c3ebf-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="c3ebf-127">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="c3ebf-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="c3ebf-128">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="c3ebf-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="c3ebf-129">Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="c3ebf-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3ebf-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c3ebf-130">See also</span></span>

- [<span data-ttu-id="c3ebf-131">XML для действий</span><span class="sxs-lookup"><span data-stu-id="c3ebf-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="c3ebf-132">Outlook Схема поставщика социальных соединителем XML</span><span class="sxs-lookup"><span data-stu-id="c3ebf-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="c3ebf-133">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="c3ebf-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

