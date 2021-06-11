---
title: элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails сохраняет необработанные данные для одного элемента ленты действий. Каждый элемент ленты действий должен иметь свой элемент activityDetails. Данные в элементе activityDetails ссылаются в шаблонах действий с помощью элементов имен.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434874"
---
# <a name="activitydetails-element"></a><span data-ttu-id="c0adc-105">элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="c0adc-105">activityDetails Element</span></span>

<span data-ttu-id="c0adc-106">Элемент **activityDetails сохраняет** необработанные данные для одного элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c0adc-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="c0adc-107">Каждый элемент ленты действий должен иметь свой **элемент activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="c0adc-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="c0adc-108">Данные в **элементе activityDetails** ссылаются в шаблонах действий с помощью **элементов имен.**</span><span class="sxs-lookup"><span data-stu-id="c0adc-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="c0adc-109">Каждый элемент данных в **элементе activityDetails должен** иметь **элемент name.**</span><span class="sxs-lookup"><span data-stu-id="c0adc-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="c0adc-110">В следующей таблице описываются шесть элементов, необходимых **элементу activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="c0adc-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="c0adc-111">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c0adc-111">**Element**</span></span>|<span data-ttu-id="c0adc-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0adc-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0adc-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="c0adc-113">**ownerID**</span></span> <br/> |<span data-ttu-id="c0adc-114">ID пользователя в социальной сети, сгенерившего этот элемент ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c0adc-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="c0adc-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="c0adc-115">**objectID**</span></span> <br/> |<span data-ttu-id="c0adc-116">Уникальная строка для элемента ленты действий для обнаружения дублирующих элементов каналов.</span><span class="sxs-lookup"><span data-stu-id="c0adc-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="c0adc-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="c0adc-117">**applicationId**</span></span> <br/> |<span data-ttu-id="c0adc-118">Один из двух уникальных ИД, используемых для совпадения элемента ленты действий с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="c0adc-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="c0adc-119">Если у вас несколько приложений или других групп, это можно использовать в качестве организатора шаблонов первого уровня.</span><span class="sxs-lookup"><span data-stu-id="c0adc-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="c0adc-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="c0adc-120">**templateId**</span></span> <br/> |<span data-ttu-id="c0adc-121">Второй уникальный ID, используемый для совпадения элемента ленты действий с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="c0adc-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="c0adc-122">Это можно использовать в качестве организатора шаблонов второго уровня.</span><span class="sxs-lookup"><span data-stu-id="c0adc-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="c0adc-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="c0adc-123">**publishDate**</span></span> <br/> |<span data-ttu-id="c0adc-124">Дата и время публикации элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c0adc-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="c0adc-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="c0adc-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="c0adc-126">Данные, которые будут использоваться в маркерах для шаблона элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="c0adc-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="c0adc-127">Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="c0adc-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0adc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c0adc-128">See also</span></span>

- [<span data-ttu-id="c0adc-129">Обзор XML для элемента ленты действий</span><span class="sxs-lookup"><span data-stu-id="c0adc-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="c0adc-130">элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="c0adc-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="c0adc-131">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="c0adc-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="c0adc-132">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="c0adc-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="c0adc-133">XML для действий</span><span class="sxs-lookup"><span data-stu-id="c0adc-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="c0adc-134">Outlook Схема поставщика социальных соединителем XML</span><span class="sxs-lookup"><span data-stu-id="c0adc-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="c0adc-135">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="c0adc-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

