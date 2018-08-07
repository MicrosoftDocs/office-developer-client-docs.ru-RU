---
title: Обзор XML для элемента веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Веб-канал активности содержит одну или несколько операций, когда социальные сети. Каждый веб-канал активности представленный элементом activityFeed и особенностями этих трех видов информации:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812849"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="66536-104">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="66536-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="66536-105">Веб-канал активности содержит одну или несколько операций, когда социальные сети.</span><span class="sxs-lookup"><span data-stu-id="66536-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="66536-106">Каждый веб-канал активности представленный элементом **activityFeed** и особенностями этих трех видов информации:</span><span class="sxs-lookup"><span data-stu-id="66536-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="66536-107">**сеть**— имя социальной сети, из которого была создана действия.</span><span class="sxs-lookup"><span data-stu-id="66536-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="66536-108">**действия**— контейнер для мероприятий, что происходит на учетную запись пользователя, выполнившего вход на этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="66536-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="66536-109">**Шаблоны**— контейнер для шаблонов, которые используются для отображения соответствующих элементов активности в **мероприятиях**.</span><span class="sxs-lookup"><span data-stu-id="66536-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="66536-110">Чтобы создать элемент веб-канала активности, должен соответствовать типу схемы XML расширяемость поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="66536-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="66536-111">На рисунке 1 показано, что XML-структура веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="66536-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="66536-112">**На рисунке 1. XML-структура веб-канала активности**</span><span class="sxs-lookup"><span data-stu-id="66536-112">**Figure 1. Activity feed XML structure**</span></span>

![XML-структура новостей](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="66536-114">Для каждого веб-канал элементов активности две наиболее важные части этой схемы представляют собой элементы **activityDetails** и **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="66536-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="66536-115">Элемент **activityDetails** хранит сведения, относящиеся к каждого элемента, такие как имя владельца активности или URL-адрес для загрузить рисунки канале активности.</span><span class="sxs-lookup"><span data-stu-id="66536-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="66536-116">Элемент **activityTemplateContainer** содержит формата или макета для каждого действия элемента веб-канала.</span><span class="sxs-lookup"><span data-stu-id="66536-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="66536-117">Он состоит из шаблонов, представленных элементами отдельных **activityTemplate** , которые могут повторно использоваться для нескольких элементов веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="66536-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="66536-118">Отдельные действия веб-канала элемента элемент **activityTemplate** указывает четыре следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="66536-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="66536-119">**значок**— указывает URL-адрес значка для отображения для действия элемента веб-канала.</span><span class="sxs-lookup"><span data-stu-id="66536-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="66536-120">**заголовок**, описание веб-канал элементов активности.</span><span class="sxs-lookup"><span data-stu-id="66536-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="66536-121">**Тип**— тип создаваемого действия, такие как состояние, фотографии или обновление документа.</span><span class="sxs-lookup"><span data-stu-id="66536-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="66536-122">**данные**— указывает любые дополнительные сведения, отображаемые с веб-канал элементов активности.</span><span class="sxs-lookup"><span data-stu-id="66536-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="66536-123">Значок, отображаемый в веб-канал активности всегда совпадает значок поставщика, возвращаемой свойством **ISocialProvider::SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="66536-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="66536-124">В следующих разделах Дополнительные сведения об элементе **activityDetails** **activityTemplateContainer** элемент, маркеры шаблона и переменные шаблона:</span><span class="sxs-lookup"><span data-stu-id="66536-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="66536-125">activityDetails элемент</span><span class="sxs-lookup"><span data-stu-id="66536-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="66536-126">activityTemplateContainer элемент</span><span class="sxs-lookup"><span data-stu-id="66536-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="66536-127">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="66536-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="66536-128">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="66536-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="66536-129">Пример активности веб-канала XML, пример [XML веб-канала активности](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="66536-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66536-130">См. также</span><span class="sxs-lookup"><span data-stu-id="66536-130">See also</span></span>

- [<span data-ttu-id="66536-131">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="66536-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="66536-132">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="66536-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="66536-133">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="66536-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

