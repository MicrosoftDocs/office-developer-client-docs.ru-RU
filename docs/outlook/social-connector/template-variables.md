---
title: Переменные шаблонов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Экземпляры переменные шаблона (представленного элементом templateVariable) укажите данные для действия канала элемента в шаблон.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812860"
---
# <a name="template-variables"></a><span data-ttu-id="b45ab-103">Переменные шаблонов</span><span class="sxs-lookup"><span data-stu-id="b45ab-103">Template variables</span></span>

<span data-ttu-id="b45ab-104">Экземпляры переменные шаблона (представленного элементом **templateVariable** ) укажите данные для действия канала элемента в шаблон.</span><span class="sxs-lookup"><span data-stu-id="b45ab-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="b45ab-105">Пример активности веб-канала XML, пример [XML веб-канала активности](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="b45ab-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="b45ab-106">В следующей таблице показаны типы переменные поддерживаемые шаблона, каждый из которых представлен соответствующее значение перечисления XML.</span><span class="sxs-lookup"><span data-stu-id="b45ab-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="b45ab-107">**Тип шаблона переменной**</span><span class="sxs-lookup"><span data-stu-id="b45ab-107">**Type of template variable**</span></span>|<span data-ttu-id="b45ab-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="b45ab-110">Лица, группы или значения.</span><span class="sxs-lookup"><span data-stu-id="b45ab-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="b45ab-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="b45ab-112">Ссылка на статью.</span><span class="sxs-lookup"><span data-stu-id="b45ab-112">A link.</span></span>  <br/> |
|<span data-ttu-id="b45ab-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-113">**listVariable**</span></span> <br/> |<span data-ttu-id="b45ab-114">Группа объектов.</span><span class="sxs-lookup"><span data-stu-id="b45ab-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="b45ab-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="b45ab-116">Изображение.</span><span class="sxs-lookup"><span data-stu-id="b45ab-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="b45ab-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="b45ab-118">Publisher действия веб-канала элемента.</span><span class="sxs-lookup"><span data-stu-id="b45ab-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="b45ab-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="b45ab-119">**textVariable**</span></span> <br/> |<span data-ttu-id="b45ab-120">Блока текста.</span><span class="sxs-lookup"><span data-stu-id="b45ab-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="b45ab-121">Каждый тип переменной шаблон обязательные элементы для определения данных об этой переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="b45ab-122">Переменные шаблона задаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b45ab-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="b45ab-123">Переменные шаблона списка</span><span class="sxs-lookup"><span data-stu-id="b45ab-123">List template variable</span></span>

<span data-ttu-id="b45ab-124">Можно указать переменные, которые содержатся в список (с разделителями элементов **listVariable** и **listItems** ) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b45ab-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="b45ab-125">Шаблон переменной типа **listVariable** является контейнером для объектов.</span><span class="sxs-lookup"><span data-stu-id="b45ab-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="b45ab-126">Он может содержать разделители запятые элементов ( **linkVariable** или **textVariable** типа) или фотографии (типа **pictureVariable** ).</span><span class="sxs-lookup"><span data-stu-id="b45ab-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="b45ab-127">Списки может содержать до пяти связать элементы, пять элементов текста или пять изображений.</span><span class="sxs-lookup"><span data-stu-id="b45ab-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="b45ab-128">Outlook Social Connector (OSC) есть перевод ссылку или текст элементов списка в соответствии с языковой стандарт системы Windows.</span><span class="sxs-lookup"><span data-stu-id="b45ab-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="b45ab-129">Чтобы правильно синтаксического анализа и отображения изображений в элемент веб-канала активности, необходимо включить изображения в список.</span><span class="sxs-lookup"><span data-stu-id="b45ab-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="b45ab-130">Все изображения изменяются 52 пикселов.</span><span class="sxs-lookup"><span data-stu-id="b45ab-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="b45ab-131">Ширина изображения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b45ab-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="b45ab-132">Элементы переменной шаблона</span><span class="sxs-lookup"><span data-stu-id="b45ab-132">Template variable elements</span></span>

<span data-ttu-id="b45ab-133">В этом разделе описываются обязательные и дополнительные элементы, поддерживаемые для каждого типа переменной шаблона.</span><span class="sxs-lookup"><span data-stu-id="b45ab-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="b45ab-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-134">entityVariable</span></span>

|<span data-ttu-id="b45ab-135">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-135">**Element**</span></span>|<span data-ttu-id="b45ab-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-137">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-137">**name**</span></span> <br/> |<span data-ttu-id="b45ab-138">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-138">The name of the variable.</span></span> <span data-ttu-id="b45ab-139">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-139">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-140">**id**</span><span class="sxs-lookup"><span data-stu-id="b45ab-140">**id**</span></span> <br/> |<span data-ttu-id="b45ab-141">Уникальный идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="b45ab-141">The unique ID of the user.</span></span> <span data-ttu-id="b45ab-142">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-142">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="b45ab-143">**nameHint**</span></span> <br/> |<span data-ttu-id="b45ab-144">Имя будет отображаться в веб-канала активности элемента.</span><span class="sxs-lookup"><span data-stu-id="b45ab-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="b45ab-145">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="b45ab-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="b45ab-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="b45ab-147">URL-адрес профиля пользователя, который будет использоваться как гиперссылки для его имя в веб-канала активности элемента при наличии его имя.</span><span class="sxs-lookup"><span data-stu-id="b45ab-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="b45ab-148">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="b45ab-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="b45ab-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="b45ab-150">Адрес электронной почты, которая позволяет обновить контактные данные этого пользователя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="b45ab-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="b45ab-151">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="b45ab-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-152">linkVariable</span></span>

|<span data-ttu-id="b45ab-153">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-153">**Element**</span></span>|<span data-ttu-id="b45ab-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-155">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-155">**name**</span></span> <br/> |<span data-ttu-id="b45ab-156">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-156">The name of the variable.</span></span> <span data-ttu-id="b45ab-157">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-157">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-158">**value**</span><span class="sxs-lookup"><span data-stu-id="b45ab-158">**value**</span></span> <br/> |<span data-ttu-id="b45ab-159">URL-адрес для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="b45ab-159">The URL for this link.</span></span> <span data-ttu-id="b45ab-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-160">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-161">**text**</span><span class="sxs-lookup"><span data-stu-id="b45ab-161">**text**</span></span> <br/> |<span data-ttu-id="b45ab-162">Текст ссылки для отображения вместо самого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b45ab-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="b45ab-163">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="b45ab-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-164">listVariable</span></span>

|<span data-ttu-id="b45ab-165">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-165">**Element**</span></span>|<span data-ttu-id="b45ab-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-167">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-167">**name**</span></span> <br/> |<span data-ttu-id="b45ab-168">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-168">The name of the variable.</span></span> <span data-ttu-id="b45ab-169">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-169">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="b45ab-170">**listItems**</span></span> <br/> |<span data-ttu-id="b45ab-171">Контейнер для элементов списка.</span><span class="sxs-lookup"><span data-stu-id="b45ab-171">A container for items in the list.</span></span> <span data-ttu-id="b45ab-172">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="b45ab-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-173">pictureVariable</span></span>

|<span data-ttu-id="b45ab-174">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-174">**Element**</span></span>|<span data-ttu-id="b45ab-175">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-176">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-176">**name**</span></span> <br/> |<span data-ttu-id="b45ab-177">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-177">The name of the variable.</span></span> <span data-ttu-id="b45ab-178">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-178">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-179">**value**</span><span class="sxs-lookup"><span data-stu-id="b45ab-179">**value**</span></span> <br/> |<span data-ttu-id="b45ab-180">URL-адрес изображения.</span><span class="sxs-lookup"><span data-stu-id="b45ab-180">The URL for the picture.</span></span> <span data-ttu-id="b45ab-181">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-181">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="b45ab-182">**altText**</span></span> <br/> |<span data-ttu-id="b45ab-183">Альтернативный текст для отображения для специальных возможностей и при наведении указателя мыши на изображение.</span><span class="sxs-lookup"><span data-stu-id="b45ab-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="b45ab-184">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="b45ab-185">**href**</span><span class="sxs-lookup"><span data-stu-id="b45ab-185">**href**</span></span> <br/> |<span data-ttu-id="b45ab-186">Гиперссылка для использования при щелчке рисунка, если нужный целевой объект не является URL-адрес изображения, заданный элементом **значение** .</span><span class="sxs-lookup"><span data-stu-id="b45ab-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="b45ab-187">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="b45ab-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-188">publisherVariable</span></span>

|<span data-ttu-id="b45ab-189">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-189">**Element**</span></span>|<span data-ttu-id="b45ab-190">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-191">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-191">**name**</span></span> <br/> |<span data-ttu-id="b45ab-192">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-192">The name of the variable.</span></span> <span data-ttu-id="b45ab-193">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-193">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-194">**id**</span><span class="sxs-lookup"><span data-stu-id="b45ab-194">**id**</span></span> <br/> |<span data-ttu-id="b45ab-195">Уникальный идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="b45ab-195">The unique ID of the user.</span></span> <span data-ttu-id="b45ab-196">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-196">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="b45ab-197">**nameHint**</span></span> <br/> |<span data-ttu-id="b45ab-198">Имя будет отображаться в веб-канала активности элемента.</span><span class="sxs-lookup"><span data-stu-id="b45ab-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="b45ab-199">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="b45ab-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="b45ab-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="b45ab-201">URL-адрес профиля пользователя, который будет использоваться как гиперссылки для его имя в веб-канала активности элемента при наличии его имя.</span><span class="sxs-lookup"><span data-stu-id="b45ab-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="b45ab-202">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="b45ab-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="b45ab-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="b45ab-204">Адрес электронной почты, которая позволяет обновить контактные данные этого пользователя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="b45ab-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="b45ab-205">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="b45ab-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="b45ab-206">textVariable</span></span>

|<span data-ttu-id="b45ab-207">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b45ab-207">**Element**</span></span>|<span data-ttu-id="b45ab-208">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b45ab-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b45ab-209">**name**</span><span class="sxs-lookup"><span data-stu-id="b45ab-209">**name**</span></span> <br/> |<span data-ttu-id="b45ab-210">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="b45ab-210">The name of the variable.</span></span> <span data-ttu-id="b45ab-211">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b45ab-211">Required.</span></span>  <br/> |
|<span data-ttu-id="b45ab-212">**value**</span><span class="sxs-lookup"><span data-stu-id="b45ab-212">**value**</span></span> <br/> |<span data-ttu-id="b45ab-213">Текст для отображения.</span><span class="sxs-lookup"><span data-stu-id="b45ab-213">The text to display.</span></span> <span data-ttu-id="b45ab-214">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b45ab-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b45ab-215">См. также</span><span class="sxs-lookup"><span data-stu-id="b45ab-215">See also</span></span>

- [<span data-ttu-id="b45ab-216">Общие сведения о XML-код для действия элемента веб-канала</span><span class="sxs-lookup"><span data-stu-id="b45ab-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="b45ab-217">activityDetails элемент</span><span class="sxs-lookup"><span data-stu-id="b45ab-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="b45ab-218">activityTemplateContainer элемент</span><span class="sxs-lookup"><span data-stu-id="b45ab-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="b45ab-219">Рекомендации для правильного отображения действий</span><span class="sxs-lookup"><span data-stu-id="b45ab-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="b45ab-220">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="b45ab-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="b45ab-221">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b45ab-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="b45ab-222">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="b45ab-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

