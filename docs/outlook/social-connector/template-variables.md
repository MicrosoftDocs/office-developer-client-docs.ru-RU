---
title: Переменные шаблонов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Экземпляры переменных шаблонов (представленные элементом templateVariable) указывают данные элемента ленты действий в шаблоне действий.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404374"
---
# <a name="template-variables"></a><span data-ttu-id="403c9-103">Переменные шаблонов</span><span class="sxs-lookup"><span data-stu-id="403c9-103">Template variables</span></span>

<span data-ttu-id="403c9-104">Экземпляры переменных шаблонов (представленные элементом **templateVariable)** указывают данные элемента ленты действий в шаблоне действий.</span><span class="sxs-lookup"><span data-stu-id="403c9-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="403c9-105">Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="403c9-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="403c9-106">В следующей таблице показаны типы поддерживаемых переменных шаблонов, каждая из которых представлена соответствующим значением XML-индексации.</span><span class="sxs-lookup"><span data-stu-id="403c9-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="403c9-107">**Тип переменной шаблона**</span><span class="sxs-lookup"><span data-stu-id="403c9-107">**Type of template variable**</span></span>|<span data-ttu-id="403c9-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="403c9-110">Человек, группа или вещь.</span><span class="sxs-lookup"><span data-stu-id="403c9-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="403c9-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="403c9-112">Ссылка.</span><span class="sxs-lookup"><span data-stu-id="403c9-112">A link.</span></span>  <br/> |
|<span data-ttu-id="403c9-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-113">**listVariable**</span></span> <br/> |<span data-ttu-id="403c9-114">Группа объектов.</span><span class="sxs-lookup"><span data-stu-id="403c9-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="403c9-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="403c9-116">Изображение.</span><span class="sxs-lookup"><span data-stu-id="403c9-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="403c9-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="403c9-118">Издатель элемента ленты действий.</span><span class="sxs-lookup"><span data-stu-id="403c9-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="403c9-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="403c9-119">**textVariable**</span></span> <br/> |<span data-ttu-id="403c9-120">Блок текста.</span><span class="sxs-lookup"><span data-stu-id="403c9-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="403c9-121">Каждый тип переменной шаблона имеет необходимые элементы для указания данных об этой переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="403c9-122">Переменные шаблона указаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="403c9-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="403c9-123">Переменная шаблона списка</span><span class="sxs-lookup"><span data-stu-id="403c9-123">List template variable</span></span>

<span data-ttu-id="403c9-124">Можно указать переменные шаблона, содержащиеся в списке (делимитированные элементами **listVariable** и **listItems)** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="403c9-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="403c9-125">Переменная шаблона **типа listVariable** — это контейнер для объектов.</span><span class="sxs-lookup"><span data-stu-id="403c9-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="403c9-126">Он может содержать запятые элементы (типа **linkVariable** или **textVariable)** или изображения (типа **pictureVariable).**</span><span class="sxs-lookup"><span data-stu-id="403c9-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="403c9-127">Списки могут содержать до пяти элементов ссылок, пять текстовых элементов или пять изображений.</span><span class="sxs-lookup"><span data-stu-id="403c9-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="403c9-128">В Outlook social Connector (OSC) локализованы элементы списка ссылок или текстов в соответствии с Windows локальной системой.</span><span class="sxs-lookup"><span data-stu-id="403c9-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="403c9-129">Чтобы правильно разобрать и отобразить изображения в элементе ленты действий, необходимо включить изображения в список.</span><span class="sxs-lookup"><span data-stu-id="403c9-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="403c9-130">Размер всех изображений составляет 52 пикселя.</span><span class="sxs-lookup"><span data-stu-id="403c9-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="403c9-131">Ширина изображения не resized.</span><span class="sxs-lookup"><span data-stu-id="403c9-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="403c9-132">Элементы переменной шаблона</span><span class="sxs-lookup"><span data-stu-id="403c9-132">Template variable elements</span></span>

<span data-ttu-id="403c9-133">В этом разделе охватываются необходимые и необязательные элементы, поддерживаемые для каждого типа переменной шаблона.</span><span class="sxs-lookup"><span data-stu-id="403c9-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="403c9-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-134">entityVariable</span></span>

|<span data-ttu-id="403c9-135">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-135">**Element**</span></span>|<span data-ttu-id="403c9-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-137">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-137">**name**</span></span> <br/> |<span data-ttu-id="403c9-138">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-138">The name of the variable.</span></span> <span data-ttu-id="403c9-139">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-139">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-140">**id**</span><span class="sxs-lookup"><span data-stu-id="403c9-140">**id**</span></span> <br/> |<span data-ttu-id="403c9-141">Уникальный ID пользователя.</span><span class="sxs-lookup"><span data-stu-id="403c9-141">The unique ID of the user.</span></span> <span data-ttu-id="403c9-142">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-142">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="403c9-143">**nameHint**</span></span> <br/> |<span data-ttu-id="403c9-144">Имя, отображаемая в элементе ленты.</span><span class="sxs-lookup"><span data-stu-id="403c9-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="403c9-145">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="403c9-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="403c9-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="403c9-147">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе ленты, если его имя присутствует.</span><span class="sxs-lookup"><span data-stu-id="403c9-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="403c9-148">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="403c9-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="403c9-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="403c9-150">Адрес электронной почты, используемый для обновления контактных данных этого лица в Outlook.</span><span class="sxs-lookup"><span data-stu-id="403c9-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="403c9-151">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="403c9-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-152">linkVariable</span></span>

|<span data-ttu-id="403c9-153">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-153">**Element**</span></span>|<span data-ttu-id="403c9-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-155">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-155">**name**</span></span> <br/> |<span data-ttu-id="403c9-156">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-156">The name of the variable.</span></span> <span data-ttu-id="403c9-157">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-157">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-158">**value**</span><span class="sxs-lookup"><span data-stu-id="403c9-158">**value**</span></span> <br/> |<span data-ttu-id="403c9-159">URL-адрес этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="403c9-159">The URL for this link.</span></span> <span data-ttu-id="403c9-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-160">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-161">**text**</span><span class="sxs-lookup"><span data-stu-id="403c9-161">**text**</span></span> <br/> |<span data-ttu-id="403c9-162">Текст ссылки, отображаемой вместо самого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="403c9-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="403c9-163">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="403c9-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-164">listVariable</span></span>

|<span data-ttu-id="403c9-165">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-165">**Element**</span></span>|<span data-ttu-id="403c9-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-167">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-167">**name**</span></span> <br/> |<span data-ttu-id="403c9-168">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-168">The name of the variable.</span></span> <span data-ttu-id="403c9-169">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-169">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="403c9-170">**listItems**</span></span> <br/> |<span data-ttu-id="403c9-171">Контейнер для элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="403c9-171">A container for items in the list.</span></span> <span data-ttu-id="403c9-172">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="403c9-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-173">pictureVariable</span></span>

|<span data-ttu-id="403c9-174">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-174">**Element**</span></span>|<span data-ttu-id="403c9-175">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-176">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-176">**name**</span></span> <br/> |<span data-ttu-id="403c9-177">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-177">The name of the variable.</span></span> <span data-ttu-id="403c9-178">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-178">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-179">**value**</span><span class="sxs-lookup"><span data-stu-id="403c9-179">**value**</span></span> <br/> |<span data-ttu-id="403c9-180">URL-адрес для изображения.</span><span class="sxs-lookup"><span data-stu-id="403c9-180">The URL for the picture.</span></span> <span data-ttu-id="403c9-181">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-181">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="403c9-182">**altText**</span></span> <br/> |<span data-ttu-id="403c9-183">Альтернативный текст, отображаемый для доступности и когда пользователь перемещает указатель мыши по изображению.</span><span class="sxs-lookup"><span data-stu-id="403c9-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="403c9-184">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="403c9-185">**href**</span><span class="sxs-lookup"><span data-stu-id="403c9-185">**href**</span></span> <br/> |<span data-ttu-id="403c9-186">Гиперссылка, используемая при щелчке изображения пользователем, если желаемая цель не является URL-адресом изображения, указанным элементом **значения.**</span><span class="sxs-lookup"><span data-stu-id="403c9-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="403c9-187">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="403c9-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-188">publisherVariable</span></span>

|<span data-ttu-id="403c9-189">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-189">**Element**</span></span>|<span data-ttu-id="403c9-190">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-191">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-191">**name**</span></span> <br/> |<span data-ttu-id="403c9-192">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-192">The name of the variable.</span></span> <span data-ttu-id="403c9-193">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-193">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-194">**id**</span><span class="sxs-lookup"><span data-stu-id="403c9-194">**id**</span></span> <br/> |<span data-ttu-id="403c9-195">Уникальный ID пользователя.</span><span class="sxs-lookup"><span data-stu-id="403c9-195">The unique ID of the user.</span></span> <span data-ttu-id="403c9-196">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-196">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="403c9-197">**nameHint**</span></span> <br/> |<span data-ttu-id="403c9-198">Имя, отображаемая в элементе ленты.</span><span class="sxs-lookup"><span data-stu-id="403c9-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="403c9-199">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="403c9-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="403c9-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="403c9-201">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе ленты, если его имя присутствует.</span><span class="sxs-lookup"><span data-stu-id="403c9-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="403c9-202">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="403c9-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="403c9-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="403c9-204">Адрес электронной почты, используемый для обновления контактных данных этого лица в Outlook.</span><span class="sxs-lookup"><span data-stu-id="403c9-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="403c9-205">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="403c9-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="403c9-206">textVariable</span></span>

|<span data-ttu-id="403c9-207">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="403c9-207">**Element**</span></span>|<span data-ttu-id="403c9-208">**Описание**</span><span class="sxs-lookup"><span data-stu-id="403c9-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403c9-209">**name**</span><span class="sxs-lookup"><span data-stu-id="403c9-209">**name**</span></span> <br/> |<span data-ttu-id="403c9-210">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="403c9-210">The name of the variable.</span></span> <span data-ttu-id="403c9-211">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="403c9-211">Required.</span></span>  <br/> |
|<span data-ttu-id="403c9-212">**value**</span><span class="sxs-lookup"><span data-stu-id="403c9-212">**value**</span></span> <br/> |<span data-ttu-id="403c9-213">Текст для отображения.</span><span class="sxs-lookup"><span data-stu-id="403c9-213">The text to display.</span></span> <span data-ttu-id="403c9-214">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="403c9-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="403c9-215">См. также</span><span class="sxs-lookup"><span data-stu-id="403c9-215">See also</span></span>

- [<span data-ttu-id="403c9-216">Обзор XML для элемента ленты действий</span><span class="sxs-lookup"><span data-stu-id="403c9-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="403c9-217">элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="403c9-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="403c9-218">элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="403c9-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="403c9-219">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="403c9-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="403c9-220">XML для действий</span><span class="sxs-lookup"><span data-stu-id="403c9-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="403c9-221">Outlook Схема поставщика социальных соединителем XML</span><span class="sxs-lookup"><span data-stu-id="403c9-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="403c9-222">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="403c9-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

