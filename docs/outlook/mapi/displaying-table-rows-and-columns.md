---
title: Отображение строк и столбцов таблиц
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
# <a name="displaying-table-rows-and-columns"></a><span data-ttu-id="f6a68-103">Отображение строк и столбцов таблиц</span><span class="sxs-lookup"><span data-stu-id="f6a68-103">Displaying Table Rows and Columns</span></span>

  
  
<span data-ttu-id="f6a68-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f6a68-105">Страница свойства может быть использована поставщиком адресных книг, чтобы пользователи могли определять новых получателей электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f6a68-105">A property page can be used by an address book provider to enable users to define new email recipients.</span></span> 
  
<span data-ttu-id="f6a68-106">Соответствующая таблица отображения содержит четыре строки, по одному для каждого управления.</span><span class="sxs-lookup"><span data-stu-id="f6a68-106">The corresponding display table contains four rows, one for each control.</span></span> <span data-ttu-id="f6a68-107">Значения столбцов, которые указывают положение, являются следующими.</span><span class="sxs-lookup"><span data-stu-id="f6a68-107">The values for the columns that indicate position are as follows.</span></span>
  
|<span data-ttu-id="f6a68-108">**Control**</span><span class="sxs-lookup"><span data-stu-id="f6a68-108">**Control**</span></span>|<span data-ttu-id="f6a68-109">**XPOS**</span><span class="sxs-lookup"><span data-stu-id="f6a68-109">**XPOS**</span></span>|<span data-ttu-id="f6a68-110">**YPOS**</span><span class="sxs-lookup"><span data-stu-id="f6a68-110">**YPOS**</span></span>|<span data-ttu-id="f6a68-111">**DELTAX**</span><span class="sxs-lookup"><span data-stu-id="f6a68-111">**DELTAX**</span></span>|<span data-ttu-id="f6a68-112">**DELTAY**</span><span class="sxs-lookup"><span data-stu-id="f6a68-112">**DELTAY**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6a68-113">Отображение метки имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-113">Display name label</span></span>  <br/> |<span data-ttu-id="f6a68-114">14 </span><span class="sxs-lookup"><span data-stu-id="f6a68-114">14</span></span>  <br/> |<span data-ttu-id="f6a68-115">18 </span><span class="sxs-lookup"><span data-stu-id="f6a68-115">18</span></span>  <br/> |<span data-ttu-id="f6a68-116">49</span><span class="sxs-lookup"><span data-stu-id="f6a68-116">49</span></span>  <br/> |<span data-ttu-id="f6a68-117">8 </span><span class="sxs-lookup"><span data-stu-id="f6a68-117">8</span></span>  <br/> |
|<span data-ttu-id="f6a68-118">Отображение окна редактирования имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-118">Display name edit box</span></span>  <br/> |<span data-ttu-id="f6a68-119">76</span><span class="sxs-lookup"><span data-stu-id="f6a68-119">76</span></span>  <br/> |<span data-ttu-id="f6a68-120">16 </span><span class="sxs-lookup"><span data-stu-id="f6a68-120">16</span></span>  <br/> |<span data-ttu-id="f6a68-121">89</span><span class="sxs-lookup"><span data-stu-id="f6a68-121">89</span></span>  <br/> |<span data-ttu-id="f6a68-122">12 </span><span class="sxs-lookup"><span data-stu-id="f6a68-122">12</span></span>  <br/> |
|<span data-ttu-id="f6a68-123">Метка адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-123">Email address label</span></span>  <br/> |<span data-ttu-id="f6a68-124">14 </span><span class="sxs-lookup"><span data-stu-id="f6a68-124">14</span></span>  <br/> |<span data-ttu-id="f6a68-125">42</span><span class="sxs-lookup"><span data-stu-id="f6a68-125">42</span></span>  <br/> |<span data-ttu-id="f6a68-126">50</span><span class="sxs-lookup"><span data-stu-id="f6a68-126">50</span></span>  <br/> |<span data-ttu-id="f6a68-127">8 </span><span class="sxs-lookup"><span data-stu-id="f6a68-127">8</span></span>  <br/> |
|<span data-ttu-id="f6a68-128">Окно редактирования адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-128">Email address edit box</span></span>  <br/> |<span data-ttu-id="f6a68-129">76</span><span class="sxs-lookup"><span data-stu-id="f6a68-129">76</span></span>  <br/> |<span data-ttu-id="f6a68-130">40</span><span class="sxs-lookup"><span data-stu-id="f6a68-130">40</span></span>  <br/> |<span data-ttu-id="f6a68-131">89</span><span class="sxs-lookup"><span data-stu-id="f6a68-131">89</span></span>  <br/> |<span data-ttu-id="f6a68-132">12 </span><span class="sxs-lookup"><span data-stu-id="f6a68-132">12</span></span>  <br/> |
|<span data-ttu-id="f6a68-133">Флажок</span><span class="sxs-lookup"><span data-stu-id="f6a68-133">Check box</span></span>  <br/> |<span data-ttu-id="f6a68-134">14 </span><span class="sxs-lookup"><span data-stu-id="f6a68-134">14</span></span>  <br/> |<span data-ttu-id="f6a68-135">64</span><span class="sxs-lookup"><span data-stu-id="f6a68-135">64</span></span>  <br/> |<span data-ttu-id="f6a68-136">90</span><span class="sxs-lookup"><span data-stu-id="f6a68-136">90</span></span>  <br/> |<span data-ttu-id="f6a68-137">12 </span><span class="sxs-lookup"><span data-stu-id="f6a68-137">12</span></span>  <br/> |
   
<span data-ttu-id="f6a68-138">В следующей таблице предлагаются соответствующие значения для типа управления, свойства **PR_CONTROL_TYPE** [(PidTagControlType)](pidtagcontroltype-canonical-property.md)и битмаски флагов, его **PR_CONTROL_FLAGS** [(PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f6a68-138">This next table suggests appropriate values for the control's type, its **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property, and bitmask of flags, its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span>
  
|<span data-ttu-id="f6a68-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="f6a68-139">**Control**</span></span>|<span data-ttu-id="f6a68-140">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f6a68-140">**Type**</span></span>|<span data-ttu-id="f6a68-141">**Flags**</span><span class="sxs-lookup"><span data-stu-id="f6a68-141">**Flags**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6a68-142">Отображение метки имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-142">Display name label</span></span>  <br/> |<span data-ttu-id="f6a68-143">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="f6a68-143">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="f6a68-144">0</span><span class="sxs-lookup"><span data-stu-id="f6a68-144">0</span></span>  <br/> |
|<span data-ttu-id="f6a68-145">Отображение окна редактирования имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-145">Display name edit box</span></span>  <br/> |<span data-ttu-id="f6a68-146">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="f6a68-146">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="f6a68-147">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="f6a68-147">DT_EDITABLE</span></span> | <span data-ttu-id="f6a68-148">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f6a68-148">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="f6a68-149">Метка адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-149">Email address label</span></span>  <br/> |<span data-ttu-id="f6a68-150">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="f6a68-150">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="f6a68-151">0</span><span class="sxs-lookup"><span data-stu-id="f6a68-151">0</span></span>  <br/> |
|<span data-ttu-id="f6a68-152">Окно редактирования адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-152">Email address edit box</span></span>  <br/> |<span data-ttu-id="f6a68-153">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="f6a68-153">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="f6a68-154">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="f6a68-154">DT_EDITABLE</span></span> | <span data-ttu-id="f6a68-155">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f6a68-155">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="f6a68-156">Флажок</span><span class="sxs-lookup"><span data-stu-id="f6a68-156">Check box</span></span>  <br/> |<span data-ttu-id="f6a68-157">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f6a68-157">DTCT_CHECKBOX</span></span>  <br/> |<span data-ttu-id="f6a68-158">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="f6a68-158">DT_EDITABLE</span></span>  <br/> |
   
<span data-ttu-id="f6a68-159">В итоговой таблице перечислены все управления содержимым связанной структуры управления.</span><span class="sxs-lookup"><span data-stu-id="f6a68-159">The final table lists each control with the contents of its associated control structure.</span></span> <span data-ttu-id="f6a68-160">Обратите внимание, что значение для каждого из элементов управления меткой отображается в памяти непосредственно после структуры.</span><span class="sxs-lookup"><span data-stu-id="f6a68-160">Notice that the value for each of the label controls appears in memory directly following the structure.</span></span>
  
|<span data-ttu-id="f6a68-161">**Control**</span><span class="sxs-lookup"><span data-stu-id="f6a68-161">**Control**</span></span>|<span data-ttu-id="f6a68-162">**Структура**</span><span class="sxs-lookup"><span data-stu-id="f6a68-162">**Structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6a68-163">Отображение метки имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-163">Display name label</span></span>  <br/> |<span data-ttu-id="f6a68-164">{sizeof (DTBLLABEL), 0} "Отображение имени:"</span><span class="sxs-lookup"><span data-stu-id="f6a68-164">{sizeof(DTBLLABEL), 0} "Display name:"</span></span>  <br/> |
|<span data-ttu-id="f6a68-165">Отображение окна редактирования имени</span><span class="sxs-lookup"><span data-stu-id="f6a68-165">Display name edit box</span></span>  <br/> |<span data-ttu-id="f6a68-166">{sizeof (DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span><span class="sxs-lookup"><span data-stu-id="f6a68-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span></span>  <br/> |
|<span data-ttu-id="f6a68-167">Метка адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-167">Email address label</span></span>  <br/> |<span data-ttu-id="f6a68-168">{sizeof (DTBLLABEL), 0} "Адрес электронной почты:"</span><span class="sxs-lookup"><span data-stu-id="f6a68-168">{sizeof(DTBLLABEL), 0} "Email address:"</span></span>  <br/> |
|<span data-ttu-id="f6a68-169">Окно редактирования адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="f6a68-169">Email address edit box</span></span>  <br/> |<span data-ttu-id="f6a68-170">{sizeof (DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span><span class="sxs-lookup"><span data-stu-id="f6a68-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span></span>  <br/> |
|<span data-ttu-id="f6a68-171">Флажок</span><span class="sxs-lookup"><span data-stu-id="f6a68-171">Check box</span></span>  <br/> |<span data-ttu-id="f6a68-172">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f6a68-172">PR_SEND_RICH_INFO</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f6a68-173">Кнопки **OK,** **Cancel** и **Help** не включены в таблицу отображения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-173">The **OK**, **Cancel**, and **Help** buttons are not included in the display table.</span></span> <span data-ttu-id="f6a68-174">Пользовательский интерфейс может добавлять контекст в диалоговое окно, добавляя элементы управления не в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-174">The user interface can add context to a dialog box by adding controls not in the display table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6a68-175">См. также</span><span class="sxs-lookup"><span data-stu-id="f6a68-175">See also</span></span>



[<span data-ttu-id="f6a68-176">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="f6a68-176">Display Table Implementation</span></span>](display-table-implementation.md)

