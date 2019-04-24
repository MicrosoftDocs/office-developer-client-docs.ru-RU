---
title: Элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails хранит необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный элемент activityDetails. К данным в элементе activityDetails ссылаются шаблоны действий с помощью элементов name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281351"
---
# <a name="activitydetails-element"></a><span data-ttu-id="3628a-105">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="3628a-105">activityDetails Element</span></span>

<span data-ttu-id="3628a-106">Элемент **activityDetails** хранит необработанные данные для одного элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="3628a-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="3628a-107">Каждый элемент веб-канала активности должен иметь собственный элемент **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="3628a-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="3628a-108">К данным в элементе **activityDetails** ссылаются шаблоны действий с помощью элементов **Name** .</span><span class="sxs-lookup"><span data-stu-id="3628a-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="3628a-109">У каждого фрагмента данных в элементе **activityDetails** должен быть элемент **Name** .</span><span class="sxs-lookup"><span data-stu-id="3628a-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="3628a-110">В следующей таблице описываются шесть элементов, необходимых для элемента **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="3628a-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="3628a-111">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3628a-111">**Element**</span></span>|<span data-ttu-id="3628a-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3628a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3628a-113">**Овнерид**</span><span class="sxs-lookup"><span data-stu-id="3628a-113">**ownerID**</span></span> <br/> |<span data-ttu-id="3628a-114">Идентификатор пользователя в социальной сети, создавшего этот элемент веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="3628a-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="3628a-115">**ИД**</span><span class="sxs-lookup"><span data-stu-id="3628a-115">**objectID**</span></span> <br/> |<span data-ttu-id="3628a-116">Уникальная строка для элемента веб-канала активности для обнаружения повторяющихся элементов веб-канала.</span><span class="sxs-lookup"><span data-stu-id="3628a-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="3628a-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="3628a-117">**applicationId**</span></span> <br/> |<span data-ttu-id="3628a-118">Один из двух уникальных идентификаторов, которые используются для сравнения элемента канала активности с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="3628a-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="3628a-119">При наличии нескольких приложений или других групп их можно использовать в качестве организатора шаблонов первого уровня.</span><span class="sxs-lookup"><span data-stu-id="3628a-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="3628a-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="3628a-120">**templateId**</span></span> <br/> |<span data-ttu-id="3628a-121">Второй уникальный идентификатор, который используется для сравнения элемента канала активности с его шаблоном.</span><span class="sxs-lookup"><span data-stu-id="3628a-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="3628a-122">Его можно использовать в качестве организатора шаблонов второго уровня.</span><span class="sxs-lookup"><span data-stu-id="3628a-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="3628a-123">**Публишдате**</span><span class="sxs-lookup"><span data-stu-id="3628a-123">**publishDate**</span></span> <br/> |<span data-ttu-id="3628a-124">Дата и время публикации элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="3628a-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="3628a-125">**Темплатевариаблес**</span><span class="sxs-lookup"><span data-stu-id="3628a-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="3628a-126">Данные, которые будут использоваться в маркерах для шаблона элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="3628a-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="3628a-127">Пример XML-кода канала активности представлен в статье [Пример XML-канала активности](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="3628a-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3628a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3628a-128">See also</span></span>

- [<span data-ttu-id="3628a-129">Обзор XML-файла для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="3628a-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="3628a-130">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="3628a-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="3628a-131">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="3628a-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="3628a-132">Рекомендации по правильному отображению действий</span><span class="sxs-lookup"><span data-stu-id="3628a-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="3628a-133">XML для действий</span><span class="sxs-lookup"><span data-stu-id="3628a-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="3628a-134">Схема XML поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="3628a-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="3628a-135">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="3628a-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

