---
title: элемент activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Элемент activityTemplateContainer — это шаблон, который позволяет форматировать элементы ленты действий и повторно использовать XML, который указывает макет.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413719"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="cecbc-103">элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="cecbc-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="cecbc-104">Элемент **activityTemplateContainer** — это шаблон, который позволяет форматировать элементы ленты действий и повторно использовать XML, который указывает макет.</span><span class="sxs-lookup"><span data-stu-id="cecbc-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="cecbc-105">Используйте ID **(applicationID** и **templateID),** чтобы соответствовать элементу feed **(activityDetails)** шаблону **(activityTemplateContainer).**</span><span class="sxs-lookup"><span data-stu-id="cecbc-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="cecbc-106">Хранение данных макета в составе **элемента activityTemplate.**</span><span class="sxs-lookup"><span data-stu-id="cecbc-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="cecbc-107">Чтобы ссылаться на данные, извлекаемые из отдельного элемента ленты действий, используйте переменные шаблона в качестве задатчиков для получения сведений, таких как люди, ссылки и текст.</span><span class="sxs-lookup"><span data-stu-id="cecbc-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="cecbc-108">В следующей таблице описываются три элемента, необходимые **элементу activityTemplateContainer.**</span><span class="sxs-lookup"><span data-stu-id="cecbc-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="cecbc-109">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cecbc-109">**Element**</span></span>|<span data-ttu-id="cecbc-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cecbc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cecbc-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="cecbc-111">**applicationID**</span></span> <br/> |<span data-ttu-id="cecbc-112">Один из двух уникальных ИД, используемых для совпадения элемента ленты с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="cecbc-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="cecbc-113">Если у вас несколько приложений или других групп, это можно использовать в качестве организатора шаблонов первого уровня.</span><span class="sxs-lookup"><span data-stu-id="cecbc-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="cecbc-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="cecbc-114">**templateID**</span></span> <br/> |<span data-ttu-id="cecbc-115">Второй уникальный ID, который используется для совпадения элемента ленты с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="cecbc-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="cecbc-116">Это можно использовать в качестве организатора шаблонов второго уровня.</span><span class="sxs-lookup"><span data-stu-id="cecbc-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="cecbc-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="cecbc-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="cecbc-118">Макет шаблона **(значок,** **заголовок** и элементы данных) и тип действия **(элемент** типа). </span><span class="sxs-lookup"><span data-stu-id="cecbc-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="cecbc-119">В следующей таблице описываются детские элементы **activityTemplate,** описывающие макет и тип шаблона.</span><span class="sxs-lookup"><span data-stu-id="cecbc-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="cecbc-120">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cecbc-120">**Element**</span></span>|<span data-ttu-id="cecbc-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cecbc-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cecbc-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="cecbc-122">**icon**</span></span> <br/> |<span data-ttu-id="cecbc-123">Маркер ссылки, который ссылается на URL-адрес значка для этого элемента ленты.</span><span class="sxs-lookup"><span data-stu-id="cecbc-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="cecbc-124">**заголовок**</span><span class="sxs-lookup"><span data-stu-id="cecbc-124">**title**</span></span> <br/> |<span data-ttu-id="cecbc-125">Необходимые сведения для элемента ленты.</span><span class="sxs-lookup"><span data-stu-id="cecbc-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="cecbc-126">**type**</span><span class="sxs-lookup"><span data-stu-id="cecbc-126">**type**</span></span> <br/> |<span data-ttu-id="cecbc-127">Тип действия, например обновление состояния, фотографии или документа.</span><span class="sxs-lookup"><span data-stu-id="cecbc-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="cecbc-128">**data**</span><span class="sxs-lookup"><span data-stu-id="cecbc-128">**data**</span></span> <br/> |<span data-ttu-id="cecbc-129">Любые дополнительные сведения для элемента ленты, такие как изображения, текст или ссылки.</span><span class="sxs-lookup"><span data-stu-id="cecbc-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="cecbc-130">Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="cecbc-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cecbc-131">См. также</span><span class="sxs-lookup"><span data-stu-id="cecbc-131">See also</span></span>

- [<span data-ttu-id="cecbc-132">Обзор XML для элемента ленты действий</span><span class="sxs-lookup"><span data-stu-id="cecbc-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="cecbc-133">элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="cecbc-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="cecbc-134">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="cecbc-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="cecbc-135">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="cecbc-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="cecbc-136">XML для действий</span><span class="sxs-lookup"><span data-stu-id="cecbc-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="cecbc-137">Outlook Схема поставщика социальных соединителем XML</span><span class="sxs-lookup"><span data-stu-id="cecbc-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="cecbc-138">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="cecbc-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

