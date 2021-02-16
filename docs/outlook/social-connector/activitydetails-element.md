---
title: Элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails сохраняет необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный элемент activityDetails. На данные в элементе activityDetails ссылается шаблоны действий с помощью элементов name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434874"
---
# <a name="activitydetails-element"></a><span data-ttu-id="da297-105">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="da297-105">activityDetails Element</span></span>

<span data-ttu-id="da297-106">Элемент **activityDetails сохраняет** необработанные данные для одного элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="da297-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="da297-107">Каждый элемент веб-канала активности должен иметь собственный **элемент activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="da297-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="da297-108">На данные в **элементе activityDetails** ссылается шаблоны действий с помощью **элементов** name.</span><span class="sxs-lookup"><span data-stu-id="da297-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="da297-109">Каждый элемент данных в **элементе activityDetails** должен иметь **элемент name.**</span><span class="sxs-lookup"><span data-stu-id="da297-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="da297-110">В следующей таблице описываются шесть элементов, необходимых **элементу activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="da297-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="da297-111">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="da297-111">**Element**</span></span>|<span data-ttu-id="da297-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="da297-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da297-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="da297-113">**ownerID**</span></span> <br/> |<span data-ttu-id="da297-114">ИД пользователя в социальной сети, который вызвал этот элемент веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="da297-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="da297-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="da297-115">**objectID**</span></span> <br/> |<span data-ttu-id="da297-116">Уникальная строка для элемента веб-канала активности для обнаружения дублирующихся элементов веб-канала.</span><span class="sxs-lookup"><span data-stu-id="da297-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="da297-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="da297-117">**applicationId**</span></span> <br/> |<span data-ttu-id="da297-118">Один из двух уникальных ИД, используемых для совпадения элемента веб-канала активности с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="da297-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="da297-119">Если у вас несколько приложений или групп, его можно использовать в качестве организатора шаблонов первого уровня.</span><span class="sxs-lookup"><span data-stu-id="da297-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="da297-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="da297-120">**templateId**</span></span> <br/> |<span data-ttu-id="da297-121">Второй уникальный ИД, используемый для совпадения элемента веб-канала активности с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="da297-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="da297-122">Его можно использовать в качестве организатора шаблонов второго уровня.</span><span class="sxs-lookup"><span data-stu-id="da297-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="da297-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="da297-123">**publishDate**</span></span> <br/> |<span data-ttu-id="da297-124">Дата и время публикации элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="da297-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="da297-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="da297-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="da297-126">Данные, используемые в маркерах для шаблона элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="da297-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="da297-127">Пример XML-канала активности см. в [XML-примере веб-канала активности](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="da297-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da297-128">См. также</span><span class="sxs-lookup"><span data-stu-id="da297-128">See also</span></span>

- [<span data-ttu-id="da297-129">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="da297-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="da297-130">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="da297-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="da297-131">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="da297-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="da297-132">Руководство по правильному отобралку действий</span><span class="sxs-lookup"><span data-stu-id="da297-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="da297-133">XML для действий</span><span class="sxs-lookup"><span data-stu-id="da297-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="da297-134">XML-схема поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="da297-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="da297-135">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="da297-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

