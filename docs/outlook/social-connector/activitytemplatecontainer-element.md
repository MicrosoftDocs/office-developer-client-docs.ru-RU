---
title: Элемент activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Элемент activityTemplateContainer — это шаблон, который позволяет форматировать элементы веб-канала активности и повторно использовать XML,который указывает макет.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413719"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="a7ddf-103">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="a7ddf-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="a7ddf-104">Элемент **activityTemplateContainer** — это шаблон, который позволяет форматировать элементы веб-канала активности и повторно использовать XML,который указывает макет.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="a7ddf-105">Используйте IDs **(applicationID** и **templateID)** для совпадения элемента веб-канала (**activityDetails**) с шаблоном (**activityTemplateContainer).**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="a7ddf-106">Храните данные макета как часть **элемента activityTemplate.**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="a7ddf-107">Для ссылки на данные, полученные из отдельного элемента веб-канала активности, используйте переменные шаблона в качестве замещего элемента для таких сведений, как люди, ссылки и текст.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="a7ddf-108">В следующей таблице описываются три элемента, необходимые элементу **activityTemplateContainer.**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="a7ddf-109">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-109">**Element**</span></span>|<span data-ttu-id="a7ddf-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7ddf-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-111">**applicationID**</span></span> <br/> |<span data-ttu-id="a7ddf-112">Один из двух уникальных ИД, используемых для совпадения элемента веб-канала с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="a7ddf-113">Если у вас несколько приложений или групп, его можно использовать в качестве организатора шаблона первого уровня.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="a7ddf-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-114">**templateID**</span></span> <br/> |<span data-ttu-id="a7ddf-115">Второй уникальный ИД, используемый для совпадения элемента веб-канала с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="a7ddf-116">Его можно использовать в качестве организатора шаблонов второго уровня.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="a7ddf-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="a7ddf-118">Макет шаблона **(значок,** **заголовок** и элементы данных) и тип действия **(элемент type).** </span><span class="sxs-lookup"><span data-stu-id="a7ddf-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="a7ddf-119">В следующей таблице описываются элементы **activityTemplate,** которые описывают макет и тип шаблона.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="a7ddf-120">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-120">**Element**</span></span>|<span data-ttu-id="a7ddf-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7ddf-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-122">**icon**</span></span> <br/> |<span data-ttu-id="a7ddf-123">Маркер ссылки, который ссылается на URL-адрес значка для этого элемента веб-канала.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="a7ddf-124">**заголовок**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-124">**title**</span></span> <br/> |<span data-ttu-id="a7ddf-125">Необходимые сведения для элемента веб-канала.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="a7ddf-126">**тип**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-126">**type**</span></span> <br/> |<span data-ttu-id="a7ddf-127">Тип действия, например обновление состояния, фотографии или документа.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="a7ddf-128">**data**</span><span class="sxs-lookup"><span data-stu-id="a7ddf-128">**data**</span></span> <br/> |<span data-ttu-id="a7ddf-129">Любые дополнительные сведения об элементе веб-канала, такие как изображения, текст или ссылки.</span><span class="sxs-lookup"><span data-stu-id="a7ddf-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="a7ddf-130">Пример XML-канала активности см. в [XML-примере веб-канала активности](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="a7ddf-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7ddf-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a7ddf-131">See also</span></span>

- [<span data-ttu-id="a7ddf-132">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="a7ddf-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="a7ddf-133">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="a7ddf-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="a7ddf-134">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="a7ddf-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="a7ddf-135">Руководство по правильному отобралку действий</span><span class="sxs-lookup"><span data-stu-id="a7ddf-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="a7ddf-136">XML для действий</span><span class="sxs-lookup"><span data-stu-id="a7ddf-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="a7ddf-137">XML-схема поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="a7ddf-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="a7ddf-138">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="a7ddf-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

