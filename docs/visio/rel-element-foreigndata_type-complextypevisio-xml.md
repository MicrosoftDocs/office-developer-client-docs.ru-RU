---
title: Элемент Rel (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает отношение между фигурой и частью документа, содержаной данные изображения, связанные с фигурой.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542809"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="9fa7e-103">Элемент Rel (ForeignData_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9fa7e-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9fa7e-104">Указывает отношение между фигурой и частью документа, содержаной данные изображения, связанные с фигурой.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fa7e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9fa7e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fa7e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fa7e-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9fa7e-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fa7e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fa7e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fa7e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9fa7e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fa7e-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fa7e-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="9fa7e-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fa7e-113">Определение</span><span class="sxs-lookup"><span data-stu-id="9fa7e-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fa7e-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9fa7e-114">Elements and attributes</span></span>

<span data-ttu-id="9fa7e-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fa7e-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9fa7e-116">Parent elements</span></span>

|<span data-ttu-id="9fa7e-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-117">**Element**</span></span>|<span data-ttu-id="9fa7e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-118">**Type**</span></span>|<span data-ttu-id="9fa7e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fa7e-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="9fa7e-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fa7e-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="9fa7e-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fa7e-122">Указывает один экземпляр данных изображения, хранимый в документе.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fa7e-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9fa7e-123">Child elements</span></span>

<span data-ttu-id="9fa7e-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fa7e-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9fa7e-125">Attributes</span></span>

|<span data-ttu-id="9fa7e-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-126">**Attribute**</span></span>|<span data-ttu-id="9fa7e-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-127">**Type**</span></span>|<span data-ttu-id="9fa7e-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-128">**Required**</span></span>|<span data-ttu-id="9fa7e-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-129">**Description**</span></span>|<span data-ttu-id="9fa7e-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fa7e-131">r:id</span><span class="sxs-lookup"><span data-stu-id="9fa7e-131">r:id</span></span>  <br/> |<span data-ttu-id="9fa7e-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9fa7e-132">xsd:string</span></span>  <br/> <span data-ttu-id="9fa7e-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="9fa7e-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="9fa7e-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9fa7e-134">required</span></span>  <br/> |<span data-ttu-id="9fa7e-135">Указывает связь с частью.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="9fa7e-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="9fa7e-136">"rId#"</span></span>  <br/> <span data-ttu-id="9fa7e-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="9fa7e-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fa7e-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fa7e-138">Remarks</span></span>

<span data-ttu-id="9fa7e-139">Значение атрибута **r:id** должно быть **ST_RelationshipID** типом.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="9fa7e-140">Тип **ST_RelationshipID** является строкой в формате rId#, где конечным символом должно быть число.</span><span class="sxs-lookup"><span data-stu-id="9fa7e-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="9fa7e-141">Число должно быть уникальным для всех элементов того же элемента **Rel.**</span><span class="sxs-lookup"><span data-stu-id="9fa7e-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="9fa7e-142">Дополнительные сведения о типе ST_RelationshipID см. в спецификации [ISO/IEC 29500, часть 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="9fa7e-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

