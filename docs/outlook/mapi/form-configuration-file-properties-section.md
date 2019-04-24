---
title: Файл конфигурации формы — раздел [Свойства]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328107"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="d82d4-103">Файл конфигурации формы — раздел [Свойства]</span><span class="sxs-lookup"><span data-stu-id="d82d4-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="d82d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d82d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d82d4-105">Раздел **[Properties]** содержит полный набор свойств, которые форма использует и публикует; то есть свойства, которые он создает в настраиваемых сообщениях, которые клиентские приложения MAPI могут использовать при отображении столбцов, фильтрации таблиц содержимого, настройке папок результатов поиска и т. д.</span><span class="sxs-lookup"><span data-stu-id="d82d4-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="d82d4-106">Каждая запись в этом списке свойств ссылается на последующее **[Property.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="d82d4-107">_строка_ **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d82d4-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="d82d4-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="d82d4-108">**[Properties]**</span></span>
  
 <span data-ttu-id="d82d4-109">**Свойств.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-109">**Property.**</span></span> <span data-ttu-id="d82d4-110">__ =  __ строка String</span><span class="sxs-lookup"><span data-stu-id="d82d4-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="d82d4-111">Формат **свойства [.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-111">The format of a [ **Property.**</span></span> <span data-ttu-id="d82d4-112">_строка_] раздел:</span><span class="sxs-lookup"><span data-stu-id="d82d4-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="d82d4-113">**Свойств.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-113">**[Property.**</span></span> <span data-ttu-id="d82d4-114">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="d82d4-114">_string_ **]**</span></span>
  
 <span data-ttu-id="d82d4-115">**Тип** =  _Integer_</span><span class="sxs-lookup"><span data-stu-id="d82d4-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="d82d4-116">\*\*\*\* =  _GUID_ нмидпропсет</span><span class="sxs-lookup"><span data-stu-id="d82d4-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="d82d4-117">\*\*\*\* =  _Строка_ нмидстринг</span><span class="sxs-lookup"><span data-stu-id="d82d4-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="d82d4-118">\*\*\*\* =  _Целое число_ нмидинтежер</span><span class="sxs-lookup"><span data-stu-id="d82d4-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="d82d4-119">\*\*\*\* =  _Строка_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="d82d4-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="d82d4-120">\*\*\*\* =  _Целое число_ флагов</span><span class="sxs-lookup"><span data-stu-id="d82d4-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="d82d4-121">**СпеЦиалтипе** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="d82d4-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="d82d4-122">\*\*\*\* =  _Строка_ Enum1</span><span class="sxs-lookup"><span data-stu-id="d82d4-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="d82d4-123">Каждое **свойство [.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-123">Each **[Property.**</span></span> <span data-ttu-id="d82d4-124">_строка_ **]** в разделе описывается одно свойство.</span><span class="sxs-lookup"><span data-stu-id="d82d4-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="d82d4-125">Запись **Type** указывает тип свойства MAPI, например 3 (PT_I4), свойства.</span><span class="sxs-lookup"><span data-stu-id="d82d4-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="d82d4-126">Запись **нмидпропсет** является необязательной; Вместе с записью **нмидстринг** или **Нмидинтежер** , запись **нмидпропсет** предоставляет имя свойства.</span><span class="sxs-lookup"><span data-stu-id="d82d4-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="d82d4-127">**Нмидстринг** предоставляет имя свойства, в то время как **нмидинтежер** задает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="d82d4-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="d82d4-128">**Нмидстринг** и **нмидинтежер** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="d82d4-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="d82d4-129">Если этот параметр установлен, **нмидпропсет** должен содержать имя набора свойств; Если отсутствует, для **нмидпропсет** устанавливается значение по умолчанию, основанное на следующем правиле: Если **нмидинтежер** присутствует, а его значение меньше 0x8000, **нмидпропсет** имеет значение пс_мапи.</span><span class="sxs-lookup"><span data-stu-id="d82d4-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="d82d4-130">Если для параметра **нмидинтежер** задано целое число больше 0x8000 или отсутствует, **нмидпропсет** задается значением пс_публик_стрингс.</span><span class="sxs-lookup"><span data-stu-id="d82d4-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="d82d4-131">Запись **DisplayName** содержит метку для свойства.</span><span class="sxs-lookup"><span data-stu-id="d82d4-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="d82d4-132">Запись **спеЦиалтипе** , если она есть, и ненулевое значение указывает на то, что это свойство является особым.</span><span class="sxs-lookup"><span data-stu-id="d82d4-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="d82d4-133">В настоящее время определен единственный тип специального свойства: **спеЦиалтипе** = 1, который указывает строковые свойства перечисления.</span><span class="sxs-lookup"><span data-stu-id="d82d4-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="d82d4-134">Если для **спеЦиалтипе** задано значение 1, запись **Enum1** ссылается на **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="d82d4-135">_строка_ **]** раздел.</span><span class="sxs-lookup"><span data-stu-id="d82d4-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="d82d4-136">Ниже приведен пример раздела **[Properties]** и **свойства [Properties.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="d82d4-137">_строка_ **]** раздел.</span><span class="sxs-lookup"><span data-stu-id="d82d4-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="d82d4-138">В предыдущем примере запись **Enum1** ссылается на последующий **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="d82d4-139">_строка_ **]** раздел, описывающий перечисление определенного типа.</span><span class="sxs-lookup"><span data-stu-id="d82d4-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="d82d4-140">Такое перечисление связывает первое свойство в **свойстве [.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="d82d4-141">_строка_ **]** в разделе с целочисленным свойством, называемым индексом.</span><span class="sxs-lookup"><span data-stu-id="d82d4-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="d82d4-142">Такое перечисление также содержит список возможных значений, которые может предполагать набор для отображения индекса Display.</span><span class="sxs-lookup"><span data-stu-id="d82d4-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="d82d4-143">Указание типа свойства для перечисления не требуется, так как в результате определения запись **Enum1** всегда имеет тип PT_I4.</span><span class="sxs-lookup"><span data-stu-id="d82d4-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="d82d4-144">Формат для параметра **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="d82d4-145">_строка_ **]** раздел:</span><span class="sxs-lookup"><span data-stu-id="d82d4-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="d82d4-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-146">**[Enum1.**</span></span> <span data-ttu-id="d82d4-147">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="d82d4-147">_string_ **]**</span></span>
  
 <span data-ttu-id="d82d4-148">\*\*\*\* =  _GUID_ нмидпропсет</span><span class="sxs-lookup"><span data-stu-id="d82d4-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="d82d4-149">\*\*\*\* =  _Строка_ нмидстринг</span><span class="sxs-lookup"><span data-stu-id="d82d4-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="d82d4-150">\*\*\*\* =  _Целое число_ нмидинтежер</span><span class="sxs-lookup"><span data-stu-id="d82d4-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="d82d4-151">\*\*\*\* =  _Целое число_ енумкаунт</span><span class="sxs-lookup"><span data-stu-id="d82d4-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="d82d4-152">**Стоимость.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-152">**Val.**</span></span> <span data-ttu-id="d82d4-153">_Integer (целое число_ ) **. Отображаемая** =  _строка_</span><span class="sxs-lookup"><span data-stu-id="d82d4-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="d82d4-154">**Стоимость.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-154">**Val.**</span></span> <span data-ttu-id="d82d4-155">_Integer (целое число_ ) \*\*. \*\* =  _Целое число_ индекса</span><span class="sxs-lookup"><span data-stu-id="d82d4-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="d82d4-156">Ниже приведен пример определения свойства для перечислимого свойства с именем Fire опасные с возможными значениями "минимум", "средний" и "высокий".</span><span class="sxs-lookup"><span data-stu-id="d82d4-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="d82d4-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="d82d4-157">**[Enum1.**</span></span> <span data-ttu-id="d82d4-158">_строка_ **]** разделы могут использоваться приложениями для двух целей: для ускорения фильтрации свойств с помощью индекса вместо строки, а также для сортировки по порядку, отличному от буквенно-цифрового порядка строковых значений.</span><span class="sxs-lookup"><span data-stu-id="d82d4-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="d82d4-159">Например, сортировку можно выполнить на основе минимального среднего значения, а не высокого среднего.</span><span class="sxs-lookup"><span data-stu-id="d82d4-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

