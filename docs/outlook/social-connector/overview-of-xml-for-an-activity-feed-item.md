---
title: Обзор XML для элемента веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Канал активности состоит из одного или нескольких действий, происходящих в социальной сети. Каждый канал активности представлен элементом activityFeed и характеризуется следующими тремя сведениями:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439949"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="c435c-104">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="c435c-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="c435c-105">Канал активности состоит из одного или нескольких действий, происходящих в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c435c-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="c435c-106">Каждый канал активности представлен элементом **activityFeed** и характеризуется следующими тремя сведениями:</span><span class="sxs-lookup"><span data-stu-id="c435c-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="c435c-107">**Network**— имя социальной сети, из которой были созданы действия.</span><span class="sxs-lookup"><span data-stu-id="c435c-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="c435c-108">**действия**— контейнер для действий, происходящих на учетной записи пользователя, выполнившего вход в этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c435c-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="c435c-109">**Templates**— контейнер для шаблонов, которые используются для отображения соответствующего элемента Activity в **действиях**.</span><span class="sxs-lookup"><span data-stu-id="c435c-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="c435c-110">Чтобы создать элемент веб-канала активности, необходимо соответствовать XML-схеме расширяемости поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c435c-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="c435c-111">На рисунке 1 показана структура XML веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c435c-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="c435c-112">**Рис. 1. Структура XML веб-канала активности**</span><span class="sxs-lookup"><span data-stu-id="c435c-112">**Figure 1. Activity feed XML structure**</span></span>

![XML-структура новостей](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="c435c-114">Для каждого элемента веб-канала активности двумя важнейшими компонентами этой схемы являются элементы **activityDetails** и **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="c435c-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="c435c-115">Элемент **activityDetails** хранит конкретные сведения для каждого элемента веб-канала активности, например имя владельца действия или URL-адрес отправленных изображений.</span><span class="sxs-lookup"><span data-stu-id="c435c-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="c435c-116">Элемент **activityTemplateContainer** сохраняет формат или макет для каждого элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c435c-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="c435c-117">Он состоит из шаблонов, представленных отдельными элементами **активититемплате** , которые можно повторно использовать для нескольких элементов веб-каналов.</span><span class="sxs-lookup"><span data-stu-id="c435c-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="c435c-118">Для отдельного элемента веб-канала активности элемент **активититемплате** определяет следующие четыре части данных:</span><span class="sxs-lookup"><span data-stu-id="c435c-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="c435c-119">**значок**— задает URL-адрес для значка, в котором отображается элемент веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c435c-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="c435c-120">**Title**— описывает элемент веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c435c-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="c435c-121">**тип**— определяет тип действия, например состояние, фотографию или обновление документа.</span><span class="sxs-lookup"><span data-stu-id="c435c-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="c435c-122">**Data (данные**) — указывает дополнительные сведения, отображаемые с элементом веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="c435c-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="c435c-123">Значок, отображаемый в веб-канале активности, всегда совпадает со значком поставщика, возвращенным свойством **исоЦиалпровидер:: соЦиалнетворкикон** .</span><span class="sxs-lookup"><span data-stu-id="c435c-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="c435c-124">В следующих разделах приведены дополнительные сведения об элементе **activityDetails** , элементе **activityTemplateContainer** , маркере шаблона и переменных шаблона:</span><span class="sxs-lookup"><span data-stu-id="c435c-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="c435c-125">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="c435c-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="c435c-126">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="c435c-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="c435c-127">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="c435c-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="c435c-128">Рекомендации по правильному отображению действий</span><span class="sxs-lookup"><span data-stu-id="c435c-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="c435c-129">Пример XML-кода канала активности представлен в статье [Пример XML-канала активности](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="c435c-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c435c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c435c-130">See also</span></span>

- [<span data-ttu-id="c435c-131">XML для действий</span><span class="sxs-lookup"><span data-stu-id="c435c-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="c435c-132">Схема XML поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="c435c-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="c435c-133">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="c435c-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

