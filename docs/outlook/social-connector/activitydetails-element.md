---
title: activityDetails элемент
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails хранит необработанные данные для отдельного веб-канала элемента действия. Каждый веб-канал элементов активности должен иметь собственный элемент activityDetails. Данные в элементе activityDetails используется в шаблоны действий с помощью имени элементов.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812710"
---
# <a name="activitydetails-element"></a><span data-ttu-id="2c385-105">activityDetails элемент</span><span class="sxs-lookup"><span data-stu-id="2c385-105">activityDetails Element</span></span>

<span data-ttu-id="2c385-106">Элемент **activityDetails** хранит необработанные данные для отдельного веб-канала элемента действия.</span><span class="sxs-lookup"><span data-stu-id="2c385-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="2c385-107">Каждый веб-канал элементов активности должен иметь собственный элемент **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="2c385-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="2c385-108">Данные в элементе **activityDetails** используется в шаблоны действий с помощью **имени** элементов.</span><span class="sxs-lookup"><span data-stu-id="2c385-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="2c385-109">Каждый элемент данных в элементе **activityDetails** должен иметь **имя** элемента.</span><span class="sxs-lookup"><span data-stu-id="2c385-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="2c385-110">В следующей таблице описаны шесть элементов, которого требует элемент **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="2c385-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="2c385-111">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2c385-111">**Element**</span></span>|<span data-ttu-id="2c385-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2c385-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c385-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="2c385-113">**ownerID**</span></span> <br/> |<span data-ttu-id="2c385-114">Идентификатор пользователя, социальные сети, созданного действия веб-канала элемента.</span><span class="sxs-lookup"><span data-stu-id="2c385-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="2c385-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="2c385-115">**objectID**</span></span> <br/> |<span data-ttu-id="2c385-116">Уникальная строка для действия веб-канала элемента для обнаружения повторяющихся элементов веб-канала.</span><span class="sxs-lookup"><span data-stu-id="2c385-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="2c385-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="2c385-117">**applicationId**</span></span> <br/> |<span data-ttu-id="2c385-118">Один из двух уникальных идентификаторов, которые используются в соответствии с действия веб-канала элемента с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="2c385-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="2c385-119">При наличии нескольких приложений или других групп, это можно использовать в качестве шаблона первого уровня Организатор.</span><span class="sxs-lookup"><span data-stu-id="2c385-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="2c385-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="2c385-120">**templateId**</span></span> <br/> |<span data-ttu-id="2c385-121">Второй уникальный идентификатор, используемый для сопоставления для действия веб-канала элемента с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="2c385-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="2c385-122">Это можно использовать в качестве организатора шаблона второго уровня.</span><span class="sxs-lookup"><span data-stu-id="2c385-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="2c385-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="2c385-123">**publishDate**</span></span> <br/> |<span data-ttu-id="2c385-124">Дата и время элемента веб-канала активности была опубликована.</span><span class="sxs-lookup"><span data-stu-id="2c385-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="2c385-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="2c385-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="2c385-126">Данные для использования в маркеры для шаблона элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="2c385-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="2c385-127">Пример активности веб-канала XML, содержатся в [Примере XML веб-канала активности](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="2c385-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c385-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2c385-128">See also</span></span>

- [<span data-ttu-id="2c385-129">Общие сведения о XML-код для действия элемента веб-канала</span><span class="sxs-lookup"><span data-stu-id="2c385-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="2c385-130">activityTemplateContainer элемент</span><span class="sxs-lookup"><span data-stu-id="2c385-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="2c385-131">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="2c385-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="2c385-132">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="2c385-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="2c385-133">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="2c385-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="2c385-134">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="2c385-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="2c385-135">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="2c385-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

