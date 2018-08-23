---
title: 'Файл конфигурации формы: раздел [Свойства]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f25d6b2db00f5629a9bf88499f9f4e080422ac29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585649"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="fb168-103">Файл конфигурации формы: раздел [Свойства]</span><span class="sxs-lookup"><span data-stu-id="fb168-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="fb168-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb168-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb168-105">В разделе **[Свойства]** представлен полный набор свойств, которые использует формы и публикует; то есть свойства, он создает в его настраиваемого сообщения, клиент MAPI приложений можно отображения столбцов, фильтрация содержимого таблицы, Настройка папки результатов поиска и т.д.</span><span class="sxs-lookup"><span data-stu-id="fb168-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="fb168-106">Каждая запись в этом списке свойство ссылается на последующих **[свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="fb168-107">_строка_ раздел **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fb168-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="fb168-108">**[Свойства]**</span><span class="sxs-lookup"><span data-stu-id="fb168-108">**[Properties]**</span></span>
  
 <span data-ttu-id="fb168-109">**Свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-109">**Property.**</span></span> <span data-ttu-id="fb168-110">_Строка_ =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="fb168-111">Формат [ **свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-111">The format of a [ **Property.**</span></span> <span data-ttu-id="fb168-112">_string_] — Это раздел:</span><span class="sxs-lookup"><span data-stu-id="fb168-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="fb168-113">**[Свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-113">**[Property.**</span></span> <span data-ttu-id="fb168-114">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="fb168-114">_string_ **]**</span></span>
  
 <span data-ttu-id="fb168-115">**Тип** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="fb168-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="fb168-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="fb168-117">**NmidString** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="fb168-118">**NmidInteger** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="fb168-119">**Отображаемое имя** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="fb168-120">**Флаги** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="fb168-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="fb168-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="fb168-122">**Enum1** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="fb168-123">Каждый **[свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-123">Each **[Property.**</span></span> <span data-ttu-id="fb168-124">_строка_ **]** разделе описываются отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="fb168-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="fb168-125">Запись **типа** указывает тип свойства MAPI, например 3 (PT_I4), свойство.</span><span class="sxs-lookup"><span data-stu-id="fb168-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="fb168-126">Запись **NmidPropset** является необязательным; вместе с **NmidString** запись или запись **NmidInteger** запись **NmidPropset** предоставляет имя свойства.</span><span class="sxs-lookup"><span data-stu-id="fb168-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="fb168-127">**NmidString** предоставляет имя свойства, в то время как **NmidInteger** предоставляет идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="fb168-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="fb168-128">**NmidString** и **NmidInteger** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="fb168-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="fb168-129">Если задан, **NmidPropset** должны содержать имя набора свойств; Если отсутствует, **NmidPropset** задано значение по умолчанию, на основе следующие правила: Если присутствует **NmidInteger** его значение равно, меньше, чем 0x8000 **NmidPropset** задано значение PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="fb168-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="fb168-130">Если значение **NmidInteger** имеет значение целое число больше, чем 0x8000 или он отсутствует, **NmidPropset** задано значение PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="fb168-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="fb168-131">Запись **DisplayName** содержит метку для свойства.</span><span class="sxs-lookup"><span data-stu-id="fb168-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="fb168-132">Запись **SpecialType** , если этот параметр указан и ненулевое значение указывает, что это свойство специальные свойства.</span><span class="sxs-lookup"><span data-stu-id="fb168-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="fb168-133">В настоящее определенного типа только специальные свойства — это **SpecialType** = 1 задает свойства строки перечисления.</span><span class="sxs-lookup"><span data-stu-id="fb168-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="fb168-134">Если **SpecialType** задано значение 1, ссылается на запись **Enum1** **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fb168-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="fb168-135">_строка_ раздел **]** .</span><span class="sxs-lookup"><span data-stu-id="fb168-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="fb168-136">Ниже приведен пример раздела **[Свойства]** и **[свойств.**</span><span class="sxs-lookup"><span data-stu-id="fb168-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="fb168-137">_строка_ раздел **]** .</span><span class="sxs-lookup"><span data-stu-id="fb168-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="fb168-138">Запись **Enum1** в предыдущем примере ссылки на последующем **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fb168-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="fb168-139">_строка_ **]** раздела, описывающего перечисления определенного типа.</span><span class="sxs-lookup"><span data-stu-id="fb168-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="fb168-140">Такие перечисления связывает к первому свойству **[свойство.**</span><span class="sxs-lookup"><span data-stu-id="fb168-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="fb168-141">_строка_ раздел **]** с помощью свойства целого числа, называется индекса.</span><span class="sxs-lookup"><span data-stu-id="fb168-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="fb168-142">Такие перечисления также содержит список возможных значений, которые можно допустить пару отображения индекса.</span><span class="sxs-lookup"><span data-stu-id="fb168-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="fb168-143">Указание типа свойства для перечисления необязательно, так как по определению запись **Enum1** всегда имеет тип PT_I4.</span><span class="sxs-lookup"><span data-stu-id="fb168-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="fb168-144">Формат для **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fb168-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="fb168-145">_строка_ раздел **]** :</span><span class="sxs-lookup"><span data-stu-id="fb168-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="fb168-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fb168-146">**[Enum1.**</span></span> <span data-ttu-id="fb168-147">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="fb168-147">_string_ **]**</span></span>
  
 <span data-ttu-id="fb168-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="fb168-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="fb168-149">**NmidString** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="fb168-150">**NmidInteger** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="fb168-151">**EnumCount** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="fb168-152">**Функция Val.**</span><span class="sxs-lookup"><span data-stu-id="fb168-152">**Val.**</span></span> <span data-ttu-id="fb168-153">_целое число_ **. Отображение** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="fb168-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="fb168-154">**Функция Val.**</span><span class="sxs-lookup"><span data-stu-id="fb168-154">**Val.**</span></span> <span data-ttu-id="fb168-155">_целое число_ **. Индекс** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="fb168-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="fb168-156">Ниже приводится определение примере свойство для перечислимых свойств, с именем пожарной опасности с возможными значениями из низкий, средний и высокий.</span><span class="sxs-lookup"><span data-stu-id="fb168-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="fb168-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="fb168-157">**[Enum1.**</span></span> <span data-ttu-id="fb168-158">_строка_ разделы **]** можно использовать в приложениях двух целях: ускорить фильтрацию свойств с помощью индекса вместо строки и сортировка в порядке, отличном от буквенно-цифровой порядок строковых значений.</span><span class="sxs-lookup"><span data-stu-id="fb168-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="fb168-159">Например сортировку можно осуществить зависимости от порядка Low Умеренно высокий вместо порядке высоким среднего.</span><span class="sxs-lookup"><span data-stu-id="fb168-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

