---
title: Элемент PageSheet (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Указывает свойства страницы рисования, связанной с хозяином.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540618"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a><span data-ttu-id="c5f99-103">Элемент PageSheet (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5f99-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c5f99-104">Указывает свойства страницы рисования, связанной с хозяином.</span><span class="sxs-lookup"><span data-stu-id="c5f99-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5f99-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c5f99-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5f99-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c5f99-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5f99-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c5f99-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5f99-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c5f99-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5f99-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c5f99-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5f99-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5f99-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5f99-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c5f99-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c5f99-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="c5f99-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5f99-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c5f99-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5f99-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5f99-114">Elements and attributes</span></span>

<span data-ttu-id="c5f99-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c5f99-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5f99-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c5f99-116">Parent elements</span></span>

|<span data-ttu-id="c5f99-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5f99-117">**Element**</span></span>|<span data-ttu-id="c5f99-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5f99-118">**Type**</span></span>|<span data-ttu-id="c5f99-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5f99-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5f99-120">Master</span><span class="sxs-lookup"><span data-stu-id="c5f99-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c5f99-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="c5f99-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5f99-122">Указывает хозяина в документе.</span><span class="sxs-lookup"><span data-stu-id="c5f99-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5f99-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c5f99-123">Child elements</span></span>

<span data-ttu-id="c5f99-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="c5f99-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5f99-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5f99-125">Attributes</span></span>

|<span data-ttu-id="c5f99-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c5f99-126">**Attribute**</span></span>|<span data-ttu-id="c5f99-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5f99-127">**Type**</span></span>|<span data-ttu-id="c5f99-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c5f99-128">**Required**</span></span>|<span data-ttu-id="c5f99-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5f99-129">**Description**</span></span>|<span data-ttu-id="c5f99-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c5f99-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5f99-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="c5f99-131">FillStyle</span></span>  <br/> |<span data-ttu-id="c5f99-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5f99-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5f99-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5f99-133">optional</span></span>  <br/> |<span data-ttu-id="c5f99-134">указывает ИД таблицы стилей, от которой необходимо наследовать форматирование заливки.</span><span class="sxs-lookup"><span data-stu-id="c5f99-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="c5f99-135">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5f99-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c5f99-136">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5f99-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5f99-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="c5f99-137">LineStyle</span></span>  <br/> |<span data-ttu-id="c5f99-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5f99-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5f99-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5f99-139">optional</span></span>  <br/> |<span data-ttu-id="c5f99-140">Указывает ИД таблицы стилей, от которой необходимо наследовать форматирование строк.</span><span class="sxs-lookup"><span data-stu-id="c5f99-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="c5f99-141">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5f99-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c5f99-142">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5f99-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5f99-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="c5f99-143">TextStyle</span></span>  <br/> |<span data-ttu-id="c5f99-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5f99-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5f99-145">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5f99-145">optional</span></span>  <br/> |<span data-ttu-id="c5f99-146">Указывает ИД таблицы стилей, от которой требуется наследовать форматирование текста.</span><span class="sxs-lookup"><span data-stu-id="c5f99-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="c5f99-147">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5f99-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c5f99-148">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5f99-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5f99-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c5f99-149">UniqueID</span></span>  <br/> |<span data-ttu-id="c5f99-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5f99-150">xsd:string</span></span>  <br/> |<span data-ttu-id="c5f99-151">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5f99-151">optional</span></span>  <br/> |<span data-ttu-id="c5f99-152">Уникальный ИД элемента в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="c5f99-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="c5f99-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5f99-153">Values of the xsd:string type.</span></span>  <br/> |
   

