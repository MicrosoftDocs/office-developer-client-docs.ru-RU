---
title: Переменные шаблонов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Экземпляры переменных шаблона (представленные элементом Темплатевариабле) указывают данные элемента веб-канала активности в шаблоне действия.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329178"
---
# <a name="template-variables"></a><span data-ttu-id="20d21-103">Переменные шаблонов</span><span class="sxs-lookup"><span data-stu-id="20d21-103">Template variables</span></span>

<span data-ttu-id="20d21-104">Экземпляры переменных шаблона (представленные элементом **темплатевариабле** ) указывают данные элемента веб-канала активности в шаблоне действия.</span><span class="sxs-lookup"><span data-stu-id="20d21-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="20d21-105">Пример XML-кода канала активности представлен в статье [Пример XML-канала активности](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="20d21-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="20d21-106">В следующей таблице приведены типы поддерживаемых переменных шаблонов, каждый из которых представлен соответствующим значением перечисления XML.</span><span class="sxs-lookup"><span data-stu-id="20d21-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="20d21-107">**Тип переменной шаблона**</span><span class="sxs-lookup"><span data-stu-id="20d21-107">**Type of template variable**</span></span>|<span data-ttu-id="20d21-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-109">**Ентитивариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="20d21-110">Пользователь, группа или вещь.</span><span class="sxs-lookup"><span data-stu-id="20d21-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="20d21-111">**Линквариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="20d21-112">Ссылка.</span><span class="sxs-lookup"><span data-stu-id="20d21-112">A link.</span></span>  <br/> |
|<span data-ttu-id="20d21-113">**Листвариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-113">**listVariable**</span></span> <br/> |<span data-ttu-id="20d21-114">Группа объектов.</span><span class="sxs-lookup"><span data-stu-id="20d21-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="20d21-115">**Пиктуревариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="20d21-116">Изображение.</span><span class="sxs-lookup"><span data-stu-id="20d21-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="20d21-117">**Публишервариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="20d21-118">Издатель элемента веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="20d21-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="20d21-119">**Текствариабле**</span><span class="sxs-lookup"><span data-stu-id="20d21-119">**textVariable**</span></span> <br/> |<span data-ttu-id="20d21-120">Блок текста.</span><span class="sxs-lookup"><span data-stu-id="20d21-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="20d21-121">Каждый тип переменной шаблона содержит обязательные элементы для указания данных об этой переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="20d21-122">Переменные шаблона задаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20d21-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="20d21-123">Переменная шаблона списка</span><span class="sxs-lookup"><span data-stu-id="20d21-123">List template variable</span></span>

<span data-ttu-id="20d21-124">Вы можете указать переменные шаблона, содержащиеся в списке (с разделителем элементами **листвариабле** и **ListItems** ), следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20d21-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="20d21-125">Переменная шаблона типа **листвариабле** является контейнером для объектов.</span><span class="sxs-lookup"><span data-stu-id="20d21-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="20d21-126">Он может содержать элементы с разделителями-запятыми (тип **линквариабле** или **текствариабле** ) или изображения (из типа **пиктуревариабле** ).</span><span class="sxs-lookup"><span data-stu-id="20d21-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="20d21-127">Списки могут содержать до пяти элементов компоновки, пяти элементов текста или пяти изображений.</span><span class="sxs-lookup"><span data-stu-id="20d21-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="20d21-128">Outlook Social Connector (OSC) локализуется элементы Link или Text List в соответствии с региональными параметрами системы Windows.</span><span class="sxs-lookup"><span data-stu-id="20d21-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="20d21-129">Чтобы правильно анализировать и отображать изображения в элементе ленты активности, необходимо включить изображения в список.</span><span class="sxs-lookup"><span data-stu-id="20d21-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="20d21-130">Размеры всех изображений изменяются в высоту 52 пикселей.</span><span class="sxs-lookup"><span data-stu-id="20d21-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="20d21-131">Ширина изображения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="20d21-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="20d21-132">Элементы переменных шаблона</span><span class="sxs-lookup"><span data-stu-id="20d21-132">Template variable elements</span></span>

<span data-ttu-id="20d21-133">В этом разделе описываются обязательные и необязательные элементы, поддерживаемые для каждого типа переменных шаблона.</span><span class="sxs-lookup"><span data-stu-id="20d21-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="20d21-134">Ентитивариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-134">entityVariable</span></span>

|<span data-ttu-id="20d21-135">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-135">**Element**</span></span>|<span data-ttu-id="20d21-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-137">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-137">**name**</span></span> <br/> |<span data-ttu-id="20d21-138">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-138">The name of the variable.</span></span> <span data-ttu-id="20d21-139">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-139">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-140">**id**</span><span class="sxs-lookup"><span data-stu-id="20d21-140">**id**</span></span> <br/> |<span data-ttu-id="20d21-141">Уникальный идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="20d21-141">The unique ID of the user.</span></span> <span data-ttu-id="20d21-142">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-142">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-143">**Намехинт**</span><span class="sxs-lookup"><span data-stu-id="20d21-143">**nameHint**</span></span> <br/> |<span data-ttu-id="20d21-144">Имя, отображаемое в элементе веб-канала.</span><span class="sxs-lookup"><span data-stu-id="20d21-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="20d21-145">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="20d21-146">**Профилеурл**</span><span class="sxs-lookup"><span data-stu-id="20d21-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="20d21-147">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе веб-канала, если имя пользователя присутствует.</span><span class="sxs-lookup"><span data-stu-id="20d21-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="20d21-148">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="20d21-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="20d21-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="20d21-150">Адрес электронной почты, который используется для обновления контактных данных этого пользователя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="20d21-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="20d21-151">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="20d21-152">Линквариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-152">linkVariable</span></span>

|<span data-ttu-id="20d21-153">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-153">**Element**</span></span>|<span data-ttu-id="20d21-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-155">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-155">**name**</span></span> <br/> |<span data-ttu-id="20d21-156">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-156">The name of the variable.</span></span> <span data-ttu-id="20d21-157">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-157">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-158">**value**</span><span class="sxs-lookup"><span data-stu-id="20d21-158">**value**</span></span> <br/> |<span data-ttu-id="20d21-159">URL-адрес для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="20d21-159">The URL for this link.</span></span> <span data-ttu-id="20d21-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-160">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-161">**text**</span><span class="sxs-lookup"><span data-stu-id="20d21-161">**text**</span></span> <br/> |<span data-ttu-id="20d21-162">Текст ссылки для отображения вместо самого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="20d21-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="20d21-163">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="20d21-164">Листвариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-164">listVariable</span></span>

|<span data-ttu-id="20d21-165">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-165">**Element**</span></span>|<span data-ttu-id="20d21-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-167">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-167">**name**</span></span> <br/> |<span data-ttu-id="20d21-168">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-168">The name of the variable.</span></span> <span data-ttu-id="20d21-169">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-169">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="20d21-170">**listItems**</span></span> <br/> |<span data-ttu-id="20d21-171">Контейнер для элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="20d21-171">A container for items in the list.</span></span> <span data-ttu-id="20d21-172">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="20d21-173">Пиктуревариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-173">pictureVariable</span></span>

|<span data-ttu-id="20d21-174">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-174">**Element**</span></span>|<span data-ttu-id="20d21-175">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-176">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-176">**name**</span></span> <br/> |<span data-ttu-id="20d21-177">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-177">The name of the variable.</span></span> <span data-ttu-id="20d21-178">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-178">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-179">**value**</span><span class="sxs-lookup"><span data-stu-id="20d21-179">**value**</span></span> <br/> |<span data-ttu-id="20d21-180">URL-адрес изображения.</span><span class="sxs-lookup"><span data-stu-id="20d21-180">The URL for the picture.</span></span> <span data-ttu-id="20d21-181">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-181">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-182">**Алттекст**</span><span class="sxs-lookup"><span data-stu-id="20d21-182">**altText**</span></span> <br/> |<span data-ttu-id="20d21-183">Альтернативный текст, отображаемый для специальных возможностей и когда пользователь наводит указатель мыши на картинку.</span><span class="sxs-lookup"><span data-stu-id="20d21-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="20d21-184">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="20d21-185">**href**</span><span class="sxs-lookup"><span data-stu-id="20d21-185">**href**</span></span> <br/> |<span data-ttu-id="20d21-186">Гиперссылка, используемая, когда пользователь щелкает изображение, если требуемый целевой объект не является URL-АДРЕСом изображения, указанным элементом **value** .</span><span class="sxs-lookup"><span data-stu-id="20d21-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="20d21-187">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="20d21-188">Публишервариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-188">publisherVariable</span></span>

|<span data-ttu-id="20d21-189">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-189">**Element**</span></span>|<span data-ttu-id="20d21-190">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-191">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-191">**name**</span></span> <br/> |<span data-ttu-id="20d21-192">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-192">The name of the variable.</span></span> <span data-ttu-id="20d21-193">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-193">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-194">**id**</span><span class="sxs-lookup"><span data-stu-id="20d21-194">**id**</span></span> <br/> |<span data-ttu-id="20d21-195">Уникальный идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="20d21-195">The unique ID of the user.</span></span> <span data-ttu-id="20d21-196">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-196">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-197">**Намехинт**</span><span class="sxs-lookup"><span data-stu-id="20d21-197">**nameHint**</span></span> <br/> |<span data-ttu-id="20d21-198">Имя, отображаемое в элементе веб-канала.</span><span class="sxs-lookup"><span data-stu-id="20d21-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="20d21-199">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="20d21-200">**Профилеурл**</span><span class="sxs-lookup"><span data-stu-id="20d21-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="20d21-201">URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе веб-канала, если имя пользователя присутствует.</span><span class="sxs-lookup"><span data-stu-id="20d21-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="20d21-202">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="20d21-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="20d21-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="20d21-204">Адрес электронной почты, который используется для обновления контактных данных этого пользователя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="20d21-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="20d21-205">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="20d21-206">Текствариабле</span><span class="sxs-lookup"><span data-stu-id="20d21-206">textVariable</span></span>

|<span data-ttu-id="20d21-207">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20d21-207">**Element**</span></span>|<span data-ttu-id="20d21-208">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20d21-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d21-209">**name**</span><span class="sxs-lookup"><span data-stu-id="20d21-209">**name**</span></span> <br/> |<span data-ttu-id="20d21-210">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="20d21-210">The name of the variable.</span></span> <span data-ttu-id="20d21-211">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20d21-211">Required.</span></span>  <br/> |
|<span data-ttu-id="20d21-212">**value**</span><span class="sxs-lookup"><span data-stu-id="20d21-212">**value**</span></span> <br/> |<span data-ttu-id="20d21-213">Отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="20d21-213">The text to display.</span></span> <span data-ttu-id="20d21-214">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="20d21-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20d21-215">См. также</span><span class="sxs-lookup"><span data-stu-id="20d21-215">See also</span></span>

- [<span data-ttu-id="20d21-216">Обзор XML-файла для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="20d21-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="20d21-217">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="20d21-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="20d21-218">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="20d21-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="20d21-219">Рекомендации по правильному отображению действий</span><span class="sxs-lookup"><span data-stu-id="20d21-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="20d21-220">XML для действий</span><span class="sxs-lookup"><span data-stu-id="20d21-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="20d21-221">Схема XML поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="20d21-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="20d21-222">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="20d21-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

