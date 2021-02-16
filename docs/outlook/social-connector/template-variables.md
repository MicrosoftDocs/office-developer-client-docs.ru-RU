---
title: Переменные шаблонов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Экземпляры переменных шаблона (представленные элементом templateVariable) указывают данные элемента веб-канала активности в шаблоне действия.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404374"
---
# <a name="template-variables"></a><span data-ttu-id="6c64b-103">Переменные шаблонов</span><span class="sxs-lookup"><span data-stu-id="6c64b-103">Template variables</span></span>

<span data-ttu-id="6c64b-104">Экземпляры переменных шаблона (представленные элементом **templateVariable)** указывают данные элемента веб-канала активности в шаблоне действия.</span><span class="sxs-lookup"><span data-stu-id="6c64b-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="6c64b-105">Пример XML-канала активности см. в [XML-примере](activity-feed-xml-example.md)веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="6c64b-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="6c64b-106">В следующей таблице показаны типы поддерживаемых переменных шаблона, каждая из которых представлена соответствующим значением измеримого XML-кода.</span><span class="sxs-lookup"><span data-stu-id="6c64b-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="6c64b-107">**Тип переменной шаблона**</span><span class="sxs-lookup"><span data-stu-id="6c64b-107">**Type of template variable**</span></span>|<span data-ttu-id="6c64b-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="6c64b-110">Человек, группа или что-то.</span><span class="sxs-lookup"><span data-stu-id="6c64b-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="6c64b-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="6c64b-112">Ссылка.</span><span class="sxs-lookup"><span data-stu-id="6c64b-112">A link.</span></span>  <br/> |
|<span data-ttu-id="6c64b-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-113">**listVariable**</span></span> <br/> |<span data-ttu-id="6c64b-114">Группа объектов.</span><span class="sxs-lookup"><span data-stu-id="6c64b-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="6c64b-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="6c64b-116">Рисунок.</span><span class="sxs-lookup"><span data-stu-id="6c64b-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="6c64b-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="6c64b-118">Издатель элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="6c64b-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="6c64b-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="6c64b-119">**textVariable**</span></span> <br/> |<span data-ttu-id="6c64b-120">Блок текста.</span><span class="sxs-lookup"><span data-stu-id="6c64b-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="6c64b-121">Каждый тип переменной шаблона имеет необходимые элементы для указания данных об этой переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="6c64b-122">Переменные шаблона указаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c64b-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="6c64b-123">Переменная шаблона списка</span><span class="sxs-lookup"><span data-stu-id="6c64b-123">List template variable</span></span>

<span data-ttu-id="6c64b-124">Можно указать переменные шаблона, содержащиеся в списке (с помощью элементов **listVariable** и **listItems),** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c64b-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="6c64b-125">Переменная шаблона типа **listVariable** является контейнером для объектов.</span><span class="sxs-lookup"><span data-stu-id="6c64b-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="6c64b-126">Он может содержать элементы с запятыми (типа **linkVariable** или **textVariable)** или изображения (типа **pictureVariable).**</span><span class="sxs-lookup"><span data-stu-id="6c64b-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="6c64b-127">Списки могут содержать до пяти элементов ссылок, пяти текстовых элементов или пяти изображений.</span><span class="sxs-lookup"><span data-stu-id="6c64b-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="6c64b-128">Outlook Social Connector (OSC) локализует элементы ссылок или текстовых списков в соответствии с региональными региональными данными системы Windows.</span><span class="sxs-lookup"><span data-stu-id="6c64b-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="6c64b-129">Для правильного разчета и отображения изображений в элементе веб-канала активности необходимо включить изображения в список.</span><span class="sxs-lookup"><span data-stu-id="6c64b-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="6c64b-130">Размер всех изображений составляет 52 пикселя.</span><span class="sxs-lookup"><span data-stu-id="6c64b-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="6c64b-131">Ширина изображения не является размером.</span><span class="sxs-lookup"><span data-stu-id="6c64b-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="6c64b-132">Элементы переменной шаблона</span><span class="sxs-lookup"><span data-stu-id="6c64b-132">Template variable elements</span></span>

<span data-ttu-id="6c64b-133">В этом разделе освещаются необходимые и необязательные элементы, поддерживаемые для каждого типа переменной шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c64b-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="6c64b-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-134">entityVariable</span></span>

|<span data-ttu-id="6c64b-135">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-135">**Element**</span></span>|<span data-ttu-id="6c64b-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-137">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-137">**name**</span></span> <br/> |<span data-ttu-id="6c64b-138">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-138">The name of the variable.</span></span> <span data-ttu-id="6c64b-139">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-139">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-140">**id**</span><span class="sxs-lookup"><span data-stu-id="6c64b-140">**id**</span></span> <br/> |<span data-ttu-id="6c64b-141">Уникальный ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c64b-141">The unique ID of the user.</span></span> <span data-ttu-id="6c64b-142">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-142">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="6c64b-143">**nameHint**</span></span> <br/> |<span data-ttu-id="6c64b-144">Имя, отображаемая в элементе веб-канала.</span><span class="sxs-lookup"><span data-stu-id="6c64b-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="6c64b-145">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="6c64b-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="6c64b-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="6c64b-147">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе веб-канала, если имя пользователя присутствует.</span><span class="sxs-lookup"><span data-stu-id="6c64b-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="6c64b-148">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="6c64b-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="6c64b-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="6c64b-150">Адрес электронной почты, используемый для обновления контактных данных этого человека в Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c64b-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="6c64b-151">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="6c64b-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-152">linkVariable</span></span>

|<span data-ttu-id="6c64b-153">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-153">**Element**</span></span>|<span data-ttu-id="6c64b-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-155">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-155">**name**</span></span> <br/> |<span data-ttu-id="6c64b-156">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-156">The name of the variable.</span></span> <span data-ttu-id="6c64b-157">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-157">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-158">**value**</span><span class="sxs-lookup"><span data-stu-id="6c64b-158">**value**</span></span> <br/> |<span data-ttu-id="6c64b-159">URL-адрес для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="6c64b-159">The URL for this link.</span></span> <span data-ttu-id="6c64b-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-160">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-161">**text**</span><span class="sxs-lookup"><span data-stu-id="6c64b-161">**text**</span></span> <br/> |<span data-ttu-id="6c64b-162">Текст ссылки, отображаемой вместо самого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="6c64b-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="6c64b-163">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="6c64b-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-164">listVariable</span></span>

|<span data-ttu-id="6c64b-165">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-165">**Element**</span></span>|<span data-ttu-id="6c64b-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-167">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-167">**name**</span></span> <br/> |<span data-ttu-id="6c64b-168">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-168">The name of the variable.</span></span> <span data-ttu-id="6c64b-169">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-169">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="6c64b-170">**listItems**</span></span> <br/> |<span data-ttu-id="6c64b-171">Контейнер для элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="6c64b-171">A container for items in the list.</span></span> <span data-ttu-id="6c64b-172">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="6c64b-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-173">pictureVariable</span></span>

|<span data-ttu-id="6c64b-174">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-174">**Element**</span></span>|<span data-ttu-id="6c64b-175">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-176">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-176">**name**</span></span> <br/> |<span data-ttu-id="6c64b-177">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-177">The name of the variable.</span></span> <span data-ttu-id="6c64b-178">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-178">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-179">**value**</span><span class="sxs-lookup"><span data-stu-id="6c64b-179">**value**</span></span> <br/> |<span data-ttu-id="6c64b-180">URL-адрес изображения.</span><span class="sxs-lookup"><span data-stu-id="6c64b-180">The URL for the picture.</span></span> <span data-ttu-id="6c64b-181">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-181">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="6c64b-182">**altText**</span></span> <br/> |<span data-ttu-id="6c64b-183">Альтернативный текст, который будет отображаться для доступности и когда пользователь нанося указатель мыши на рисунок.</span><span class="sxs-lookup"><span data-stu-id="6c64b-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="6c64b-184">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="6c64b-185">**href**</span><span class="sxs-lookup"><span data-stu-id="6c64b-185">**href**</span></span> <br/> |<span data-ttu-id="6c64b-186">Гиперссылка, используемая, когда пользователь щелкает рисунок, если нужный целевой объект не является URL-адресом изображения, указанным **элементом значения.**</span><span class="sxs-lookup"><span data-stu-id="6c64b-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="6c64b-187">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="6c64b-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-188">publisherVariable</span></span>

|<span data-ttu-id="6c64b-189">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-189">**Element**</span></span>|<span data-ttu-id="6c64b-190">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-191">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-191">**name**</span></span> <br/> |<span data-ttu-id="6c64b-192">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-192">The name of the variable.</span></span> <span data-ttu-id="6c64b-193">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-193">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-194">**id**</span><span class="sxs-lookup"><span data-stu-id="6c64b-194">**id**</span></span> <br/> |<span data-ttu-id="6c64b-195">Уникальный ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c64b-195">The unique ID of the user.</span></span> <span data-ttu-id="6c64b-196">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-196">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="6c64b-197">**nameHint**</span></span> <br/> |<span data-ttu-id="6c64b-198">Имя, отображаемая в элементе веб-канала.</span><span class="sxs-lookup"><span data-stu-id="6c64b-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="6c64b-199">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="6c64b-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="6c64b-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="6c64b-201">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе веб-канала, если имя пользователя присутствует.</span><span class="sxs-lookup"><span data-stu-id="6c64b-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="6c64b-202">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="6c64b-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="6c64b-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="6c64b-204">Адрес электронной почты, используемый для обновления контактных данных этого человека в Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c64b-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="6c64b-205">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="6c64b-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="6c64b-206">textVariable</span></span>

|<span data-ttu-id="6c64b-207">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6c64b-207">**Element**</span></span>|<span data-ttu-id="6c64b-208">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c64b-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c64b-209">**name**</span><span class="sxs-lookup"><span data-stu-id="6c64b-209">**name**</span></span> <br/> |<span data-ttu-id="6c64b-210">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6c64b-210">The name of the variable.</span></span> <span data-ttu-id="6c64b-211">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6c64b-211">Required.</span></span>  <br/> |
|<span data-ttu-id="6c64b-212">**value**</span><span class="sxs-lookup"><span data-stu-id="6c64b-212">**value**</span></span> <br/> |<span data-ttu-id="6c64b-213">Текст, который необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="6c64b-213">The text to display.</span></span> <span data-ttu-id="6c64b-214">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6c64b-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c64b-215">См. также</span><span class="sxs-lookup"><span data-stu-id="6c64b-215">See also</span></span>

- [<span data-ttu-id="6c64b-216">Обзор XML для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="6c64b-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="6c64b-217">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="6c64b-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="6c64b-218">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="6c64b-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="6c64b-219">Руководство по правильному отобралку действий</span><span class="sxs-lookup"><span data-stu-id="6c64b-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="6c64b-220">XML для действий</span><span class="sxs-lookup"><span data-stu-id="6c64b-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="6c64b-221">XML-схема поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="6c64b-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6c64b-222">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="6c64b-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

