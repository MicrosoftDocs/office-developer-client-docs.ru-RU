---
title: Отображение строк и столбцов таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407118"
---
# <a name="displaying-table-rows-and-columns"></a><span data-ttu-id="6271b-103">Отображение строк и столбцов таблицы</span><span class="sxs-lookup"><span data-stu-id="6271b-103">Displaying Table Rows and Columns</span></span>

  
  
<span data-ttu-id="6271b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6271b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6271b-105">Поставщик адресной книги может использовать страницу свойств, чтобы пользователи могли определять новых получателей электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6271b-105">A property page can be used by an address book provider to enable users to define new email recipients.</span></span> 
  
<span data-ttu-id="6271b-106">Соответствующая таблица отображения содержит четыре строки, по одной для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="6271b-106">The corresponding display table contains four rows, one for each control.</span></span> <span data-ttu-id="6271b-107">Значения столбцов, которые указывают позицию, указаны следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6271b-107">The values for the columns that indicate position are as follows.</span></span>
  
|<span data-ttu-id="6271b-108">**Control**</span><span class="sxs-lookup"><span data-stu-id="6271b-108">**Control**</span></span>|<span data-ttu-id="6271b-109">**XPOS**</span><span class="sxs-lookup"><span data-stu-id="6271b-109">**XPOS**</span></span>|<span data-ttu-id="6271b-110">**YPOS**</span><span class="sxs-lookup"><span data-stu-id="6271b-110">**YPOS**</span></span>|<span data-ttu-id="6271b-111">**DELTAX**</span><span class="sxs-lookup"><span data-stu-id="6271b-111">**DELTAX**</span></span>|<span data-ttu-id="6271b-112">**DELTAY**</span><span class="sxs-lookup"><span data-stu-id="6271b-112">**DELTAY**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6271b-113">Метка отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-113">Display name label</span></span>  <br/> |<span data-ttu-id="6271b-114">14 </span><span class="sxs-lookup"><span data-stu-id="6271b-114">14</span></span>  <br/> |<span data-ttu-id="6271b-115">18 </span><span class="sxs-lookup"><span data-stu-id="6271b-115">18</span></span>  <br/> |<span data-ttu-id="6271b-116">49</span><span class="sxs-lookup"><span data-stu-id="6271b-116">49</span></span>  <br/> |<span data-ttu-id="6271b-117">8 </span><span class="sxs-lookup"><span data-stu-id="6271b-117">8</span></span>  <br/> |
|<span data-ttu-id="6271b-118">Окно редактирования отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-118">Display name edit box</span></span>  <br/> |<span data-ttu-id="6271b-119">76</span><span class="sxs-lookup"><span data-stu-id="6271b-119">76</span></span>  <br/> |<span data-ttu-id="6271b-120">16 </span><span class="sxs-lookup"><span data-stu-id="6271b-120">16</span></span>  <br/> |<span data-ttu-id="6271b-121">89</span><span class="sxs-lookup"><span data-stu-id="6271b-121">89</span></span>  <br/> |<span data-ttu-id="6271b-122">12 </span><span class="sxs-lookup"><span data-stu-id="6271b-122">12</span></span>  <br/> |
|<span data-ttu-id="6271b-123">Метка адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-123">Email address label</span></span>  <br/> |<span data-ttu-id="6271b-124">14 </span><span class="sxs-lookup"><span data-stu-id="6271b-124">14</span></span>  <br/> |<span data-ttu-id="6271b-125">42</span><span class="sxs-lookup"><span data-stu-id="6271b-125">42</span></span>  <br/> |<span data-ttu-id="6271b-126">50</span><span class="sxs-lookup"><span data-stu-id="6271b-126">50</span></span>  <br/> |<span data-ttu-id="6271b-127">8 </span><span class="sxs-lookup"><span data-stu-id="6271b-127">8</span></span>  <br/> |
|<span data-ttu-id="6271b-128">Поле редактирования адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-128">Email address edit box</span></span>  <br/> |<span data-ttu-id="6271b-129">76</span><span class="sxs-lookup"><span data-stu-id="6271b-129">76</span></span>  <br/> |<span data-ttu-id="6271b-130">40</span><span class="sxs-lookup"><span data-stu-id="6271b-130">40</span></span>  <br/> |<span data-ttu-id="6271b-131">89</span><span class="sxs-lookup"><span data-stu-id="6271b-131">89</span></span>  <br/> |<span data-ttu-id="6271b-132">12 </span><span class="sxs-lookup"><span data-stu-id="6271b-132">12</span></span>  <br/> |
|<span data-ttu-id="6271b-133">Флажок</span><span class="sxs-lookup"><span data-stu-id="6271b-133">Check box</span></span>  <br/> |<span data-ttu-id="6271b-134">14 </span><span class="sxs-lookup"><span data-stu-id="6271b-134">14</span></span>  <br/> |<span data-ttu-id="6271b-135">64</span><span class="sxs-lookup"><span data-stu-id="6271b-135">64</span></span>  <br/> |<span data-ttu-id="6271b-136">90</span><span class="sxs-lookup"><span data-stu-id="6271b-136">90</span></span>  <br/> |<span data-ttu-id="6271b-137">12 </span><span class="sxs-lookup"><span data-stu-id="6271b-137">12</span></span>  <br/> |
   
<span data-ttu-id="6271b-138">В следующей таблице предлагаются соответствующие значения для типа, свойства **PR_CONTROL_TYPE** [(PidTagControlType)](pidtagcontroltype-canonical-property.md)и битовой маской флагов, его свойства **PR_CONTROL_FLAGS** ([PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6271b-138">This next table suggests appropriate values for the control's type, its **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property, and bitmask of flags, its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span>
  
|<span data-ttu-id="6271b-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="6271b-139">**Control**</span></span>|<span data-ttu-id="6271b-140">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6271b-140">**Type**</span></span>|<span data-ttu-id="6271b-141">**Flags**</span><span class="sxs-lookup"><span data-stu-id="6271b-141">**Flags**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6271b-142">Метка отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-142">Display name label</span></span>  <br/> |<span data-ttu-id="6271b-143">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="6271b-143">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="6271b-144">0</span><span class="sxs-lookup"><span data-stu-id="6271b-144">0</span></span>  <br/> |
|<span data-ttu-id="6271b-145">Окно редактирования отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-145">Display name edit box</span></span>  <br/> |<span data-ttu-id="6271b-146">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="6271b-146">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="6271b-147">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="6271b-147">DT_EDITABLE</span></span> | <span data-ttu-id="6271b-148">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6271b-148">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="6271b-149">Метка адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-149">Email address label</span></span>  <br/> |<span data-ttu-id="6271b-150">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="6271b-150">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="6271b-151">0</span><span class="sxs-lookup"><span data-stu-id="6271b-151">0</span></span>  <br/> |
|<span data-ttu-id="6271b-152">Поле редактирования адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-152">Email address edit box</span></span>  <br/> |<span data-ttu-id="6271b-153">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="6271b-153">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="6271b-154">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="6271b-154">DT_EDITABLE</span></span> | <span data-ttu-id="6271b-155">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6271b-155">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="6271b-156">Флажок</span><span class="sxs-lookup"><span data-stu-id="6271b-156">Check box</span></span>  <br/> |<span data-ttu-id="6271b-157">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="6271b-157">DTCT_CHECKBOX</span></span>  <br/> |<span data-ttu-id="6271b-158">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="6271b-158">DT_EDITABLE</span></span>  <br/> |
   
<span data-ttu-id="6271b-159">В последней таблице перечисляется каждый из них с содержимым связанной с ним структуры.</span><span class="sxs-lookup"><span data-stu-id="6271b-159">The final table lists each control with the contents of its associated control structure.</span></span> <span data-ttu-id="6271b-160">Обратите внимание, что значение для каждого из элементов управления меткой отображается в памяти непосредственно после структуры.</span><span class="sxs-lookup"><span data-stu-id="6271b-160">Notice that the value for each of the label controls appears in memory directly following the structure.</span></span>
  
|<span data-ttu-id="6271b-161">**Control**</span><span class="sxs-lookup"><span data-stu-id="6271b-161">**Control**</span></span>|<span data-ttu-id="6271b-162">**Структура**</span><span class="sxs-lookup"><span data-stu-id="6271b-162">**Structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6271b-163">Метка отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-163">Display name label</span></span>  <br/> |<span data-ttu-id="6271b-164">{sizeof(DTBLLABEL), 0} "Display name:"</span><span class="sxs-lookup"><span data-stu-id="6271b-164">{sizeof(DTBLLABEL), 0} "Display name:"</span></span>  <br/> |
|<span data-ttu-id="6271b-165">Окно редактирования отображаемой имени</span><span class="sxs-lookup"><span data-stu-id="6271b-165">Display name edit box</span></span>  <br/> |<span data-ttu-id="6271b-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span><span class="sxs-lookup"><span data-stu-id="6271b-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span></span>  <br/> |
|<span data-ttu-id="6271b-167">Метка адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-167">Email address label</span></span>  <br/> |<span data-ttu-id="6271b-168">{sizeof(DTBLLABEL), 0} "Адрес электронной почты:"</span><span class="sxs-lookup"><span data-stu-id="6271b-168">{sizeof(DTBLLABEL), 0} "Email address:"</span></span>  <br/> |
|<span data-ttu-id="6271b-169">Поле редактирования адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="6271b-169">Email address edit box</span></span>  <br/> |<span data-ttu-id="6271b-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span><span class="sxs-lookup"><span data-stu-id="6271b-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span></span>  <br/> |
|<span data-ttu-id="6271b-171">Флажок</span><span class="sxs-lookup"><span data-stu-id="6271b-171">Check box</span></span>  <br/> |<span data-ttu-id="6271b-172">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="6271b-172">PR_SEND_RICH_INFO</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6271b-173">Кнопки **"ОК",** **"Отмена"** и "Справка" не включены в таблицу отображения. </span><span class="sxs-lookup"><span data-stu-id="6271b-173">The **OK**, **Cancel**, and **Help** buttons are not included in the display table.</span></span> <span data-ttu-id="6271b-174">Пользовательский интерфейс может добавлять контекст в диалоговое окно, добавляя элементы управления не в отображаемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="6271b-174">The user interface can add context to a dialog box by adding controls not in the display table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6271b-175">См. также</span><span class="sxs-lookup"><span data-stu-id="6271b-175">See also</span></span>



[<span data-ttu-id="6271b-176">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="6271b-176">Display Table Implementation</span></span>](display-table-implementation.md)

