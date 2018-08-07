---
title: activityTemplateContainer элемент
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Элемент activityTemplateContainer — это шаблон, который позволяет форматирование элементов веб-канал активности и повторного использования XML, которая определяет макет.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812713"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="d15a4-103">activityTemplateContainer элемент</span><span class="sxs-lookup"><span data-stu-id="d15a4-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="d15a4-104">Элемент **activityTemplateContainer** — это шаблон, который позволяет форматирование элементов веб-канал активности и повторного использования XML, которая определяет макет.</span><span class="sxs-lookup"><span data-stu-id="d15a4-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="d15a4-105">С помощью идентификаторов (**applicationID** и **идентификатор шаблона**) в соответствии с веб-канала активности элемента (**activityDetails**) для шаблона (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="d15a4-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="d15a4-106">Хранилища данных разметки как часть элемента **activityTemplate** .</span><span class="sxs-lookup"><span data-stu-id="d15a4-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="d15a4-107">Для данных, которые извлекаются из отдельных веб-канал элементов активности следует используйте переменные шаблона как заполнители для людей, ссылки и текст.</span><span class="sxs-lookup"><span data-stu-id="d15a4-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="d15a4-108">В следующей таблице описаны три элементы, которого требует элемент **activityTemplateContainer** .</span><span class="sxs-lookup"><span data-stu-id="d15a4-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="d15a4-109">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d15a4-109">**Element**</span></span>|<span data-ttu-id="d15a4-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d15a4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d15a4-111">**Идентификатор приложения**</span><span class="sxs-lookup"><span data-stu-id="d15a4-111">**applicationID**</span></span> <br/> |<span data-ttu-id="d15a4-112">Один из двух уникальных идентификаторов, которые используются в соответствии с веб-канала активности элемента с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="d15a4-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="d15a4-113">При наличии нескольких приложений или других групп, это можно использовать в качестве шаблона первого уровня Организатор.</span><span class="sxs-lookup"><span data-stu-id="d15a4-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="d15a4-114">**Идентификатор шаблона**</span><span class="sxs-lookup"><span data-stu-id="d15a4-114">**templateID**</span></span> <br/> |<span data-ttu-id="d15a4-115">Второй уникальный идентификатор, используемый в соответствии с веб-канала активности элемента с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="d15a4-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="d15a4-116">Это можно использовать в качестве организатора шаблона второго уровня.</span><span class="sxs-lookup"><span data-stu-id="d15a4-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="d15a4-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="d15a4-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="d15a4-118">Структура шаблона (**значок**, **заголовок**и **данные** элементы) и тип действия (элемент**type** ).</span><span class="sxs-lookup"><span data-stu-id="d15a4-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="d15a4-119">В следующей таблице описаны дочерние элементы **activityTemplate**, которые описывают макет и тип шаблона.</span><span class="sxs-lookup"><span data-stu-id="d15a4-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="d15a4-120">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d15a4-120">**Element**</span></span>|<span data-ttu-id="d15a4-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d15a4-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d15a4-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="d15a4-122">**icon**</span></span> <br/> |<span data-ttu-id="d15a4-123">Ссылка маркер, который ссылается на URL-адрес для значка для этого веб-канала активности элемента.</span><span class="sxs-lookup"><span data-stu-id="d15a4-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="d15a4-124">**title**</span><span class="sxs-lookup"><span data-stu-id="d15a4-124">**title**</span></span> <br/> |<span data-ttu-id="d15a4-125">Необходимые сведения для элемента веб-канала.</span><span class="sxs-lookup"><span data-stu-id="d15a4-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="d15a4-126">**type**</span><span class="sxs-lookup"><span data-stu-id="d15a4-126">**type**</span></span> <br/> |<span data-ttu-id="d15a4-127">Тип действия, такие как обновление состояния, фотографии или документа.</span><span class="sxs-lookup"><span data-stu-id="d15a4-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="d15a4-128">**data**</span><span class="sxs-lookup"><span data-stu-id="d15a4-128">**data**</span></span> <br/> |<span data-ttu-id="d15a4-129">Любые дополнительные сведения для веб-канала активности элемента, такие как изображения, текст и ссылки.</span><span class="sxs-lookup"><span data-stu-id="d15a4-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="d15a4-130">Пример активности веб-канала XML, содержатся в [Примере XML веб-канала активности](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="d15a4-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d15a4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d15a4-131">See also</span></span>

- [<span data-ttu-id="d15a4-132">Общие сведения о XML-код для действия элемента веб-канала</span><span class="sxs-lookup"><span data-stu-id="d15a4-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="d15a4-133">activityDetails элемент</span><span class="sxs-lookup"><span data-stu-id="d15a4-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="d15a4-134">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="d15a4-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="d15a4-135">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="d15a4-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="d15a4-136">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="d15a4-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="d15a4-137">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d15a4-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="d15a4-138">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="d15a4-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

