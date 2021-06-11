---
title: Раздел Конфигурация формы [Свойства]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421293"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="c12bb-103">Раздел Конфигурация формы [Свойства]</span><span class="sxs-lookup"><span data-stu-id="c12bb-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="c12bb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c12bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c12bb-105">В **разделе [Свойства]** перечислены полные свойства, которые форма использует и публикует; то есть свойства, которые он создает в пользовательских сообщениях, которые клиентские приложения MAPI могут использовать при отображке столбцов, фильтрации таблиц контента, настройке папок результатов поиска и т. д.</span><span class="sxs-lookup"><span data-stu-id="c12bb-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="c12bb-106">Каждая запись в этом списке свойств ссылается на **последующее [Свойство.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="c12bb-107">_строка_ **]** раздела, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c12bb-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="c12bb-108">**[Свойства]**</span><span class="sxs-lookup"><span data-stu-id="c12bb-108">**[Properties]**</span></span>
  
 <span data-ttu-id="c12bb-109">**Свойство.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-109">**Property.**</span></span> <span data-ttu-id="c12bb-110">_строка_  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="c12bb-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="c12bb-111">Формат **[Свойства.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-111">The format of a [ **Property.**</span></span> <span data-ttu-id="c12bb-112">_строка_] Раздел:</span><span class="sxs-lookup"><span data-stu-id="c12bb-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="c12bb-113">**[Свойство.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-113">**[Property.**</span></span> <span data-ttu-id="c12bb-114">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="c12bb-114">_string_ **]**</span></span>
  
 <span data-ttu-id="c12bb-115">**Тип**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="c12bb-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="c12bb-116">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="c12bb-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="c12bb-117">**NmidString**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="c12bb-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="c12bb-118">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="c12bb-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="c12bb-119">**DisplayName**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="c12bb-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="c12bb-120">**Флаги**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="c12bb-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="c12bb-121">**SpecialType** = 0|1</span><span class="sxs-lookup"><span data-stu-id="c12bb-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="c12bb-122">**Enum1**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="c12bb-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="c12bb-123">Каждое **[Свойство.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-123">Each **[Property.**</span></span> <span data-ttu-id="c12bb-124">_в_ **разделе string ]** описывается одно свойство.</span><span class="sxs-lookup"><span data-stu-id="c12bb-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="c12bb-125">В **записи** Type указывается тип свойства MAPI, например 3 (PT_I4) свойства.</span><span class="sxs-lookup"><span data-stu-id="c12bb-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="c12bb-126">Запись **NmidPropset** необязательна; Вместе с **записью NmidString** или **записью NmidInteger** запись **NmidPropset** дает имя свойства.</span><span class="sxs-lookup"><span data-stu-id="c12bb-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="c12bb-127">**NmidString** дает имя свойства, а **NmidInteger** — идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="c12bb-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="c12bb-128">**NmidString** и **NmidInteger** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="c12bb-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="c12bb-129">Если установлено, **NmidPropset** должен содержать имя набора свойств; При отсутствии **NmidPropset** устанавливается значение по умолчанию, основанное на следующем правиле: если **NmidInteger** присутствует и его значение меньше 0x8000, **NmidPropset** задан для PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="c12bb-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="c12bb-130">Если значение **NmidInteger** задано свыше 0x8000 или если оно отсутствует, **NmidPropset** задан для PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="c12bb-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="c12bb-131">Запись **DisplayName** содержит метку свойства.</span><span class="sxs-lookup"><span data-stu-id="c12bb-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="c12bb-132">Запись **SpecialType,** если она присутствует и не является, указывает на то, что это свойство является специальным свойством.</span><span class="sxs-lookup"><span data-stu-id="c12bb-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="c12bb-133">В настоящее время единственным определенным типом специального свойства является **SpecialType** = 1, который указывает на свойства строки, указанные в строке.</span><span class="sxs-lookup"><span data-stu-id="c12bb-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="c12bb-134">Если **в SpecialType** установлено 1, запись **Enum1 ссылается** на **[Enum1).**</span><span class="sxs-lookup"><span data-stu-id="c12bb-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="c12bb-135">_строка_ **]** раздела.</span><span class="sxs-lookup"><span data-stu-id="c12bb-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="c12bb-136">Ниже приводится пример **раздела [Свойства]** и **[Свойства.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="c12bb-137">_строка_ **]** раздела.</span><span class="sxs-lookup"><span data-stu-id="c12bb-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="c12bb-138">Запись **Enum1** в предварительном примере ссылается на последующий **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="c12bb-139">_строка_ **]** раздел, описывающий описание определенного типа.</span><span class="sxs-lookup"><span data-stu-id="c12bb-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="c12bb-140">Такое переумежение связывает первое свойство в **[Property.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="c12bb-141">_строка_ **]** раздела с свойством integer, называемым индексом.</span><span class="sxs-lookup"><span data-stu-id="c12bb-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="c12bb-142">Такое перечисляние также содержит список возможных значений, которые может предполагать пара display-index.</span><span class="sxs-lookup"><span data-stu-id="c12bb-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="c12bb-143">Указывать тип свойства для переумерия необязательно, так как по определению запись **Enum1** всегда имеет PT_I4 тип.</span><span class="sxs-lookup"><span data-stu-id="c12bb-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="c12bb-144">Формат **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="c12bb-145">_строка_ **]** раздел:</span><span class="sxs-lookup"><span data-stu-id="c12bb-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="c12bb-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-146">**[Enum1.**</span></span> <span data-ttu-id="c12bb-147">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="c12bb-147">_string_ **]**</span></span>
  
 <span data-ttu-id="c12bb-148">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="c12bb-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="c12bb-149">**NmidString**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="c12bb-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="c12bb-150">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="c12bb-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="c12bb-151">**EnumCount**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="c12bb-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="c12bb-152">**Вал.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-152">**Val.**</span></span> <span data-ttu-id="c12bb-153">_integer_ **. Отображение**  =   _строки_</span><span class="sxs-lookup"><span data-stu-id="c12bb-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="c12bb-154">**Вал.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-154">**Val.**</span></span> <span data-ttu-id="c12bb-155">_integer_ **. Индексация**  =   </span><span class="sxs-lookup"><span data-stu-id="c12bb-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="c12bb-156">Ниже приводится пример определения свойства для засвещенного свойства с именем Fire Hazard с возможными значениями Low, Medium и High.</span><span class="sxs-lookup"><span data-stu-id="c12bb-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="c12bb-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="c12bb-157">**[Enum1.**</span></span> <span data-ttu-id="c12bb-158">_строка_ **]** разделы могут использоваться приложениями для двух целей: для ускорения фильтрации свойств с помощью индекса вместо строки и сортировки по другому порядку, чем альфа-порядку значений строки.</span><span class="sxs-lookup"><span data-stu-id="c12bb-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="c12bb-159">Например, сортировка может быть сделана на основе порядка с низким уровнем средней и высокой высоты, а не по заказу high-Medium-Low.</span><span class="sxs-lookup"><span data-stu-id="c12bb-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

