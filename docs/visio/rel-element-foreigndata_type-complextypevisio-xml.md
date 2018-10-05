---
title: Элемент Rel (ForeignData_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383445"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="4301f-103">Элемент Rel (ForeignData_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4301f-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4301f-104">Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.</span><span class="sxs-lookup"><span data-stu-id="4301f-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4301f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4301f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4301f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4301f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4301f-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="4301f-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4301f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4301f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4301f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4301f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4301f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4301f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4301f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4301f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4301f-112">Pages.XML, masters.xml, recordsets.xml, страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="4301f-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4301f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4301f-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4301f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4301f-114">Elements and attributes</span></span>

<span data-ttu-id="4301f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4301f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4301f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4301f-116">Parent elements</span></span>

|<span data-ttu-id="4301f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4301f-117">**Element**</span></span>|<span data-ttu-id="4301f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4301f-118">**Type**</span></span>|<span data-ttu-id="4301f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4301f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4301f-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="4301f-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4301f-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="4301f-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4301f-122">Один экземпляр данных изображения, хранящиеся в документе.</span><span class="sxs-lookup"><span data-stu-id="4301f-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4301f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4301f-123">Child elements</span></span>

<span data-ttu-id="4301f-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="4301f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4301f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4301f-125">Attributes</span></span>

|<span data-ttu-id="4301f-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4301f-126">**Attribute**</span></span>|<span data-ttu-id="4301f-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4301f-127">**Type**</span></span>|<span data-ttu-id="4301f-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4301f-128">**Required**</span></span>|<span data-ttu-id="4301f-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4301f-129">**Description**</span></span>|<span data-ttu-id="4301f-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4301f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4301f-131">r: код</span><span class="sxs-lookup"><span data-stu-id="4301f-131">r:id</span></span>  <br/> |<span data-ttu-id="4301f-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="4301f-132">xsd:string</span></span>  <br/> <span data-ttu-id="4301f-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="4301f-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="4301f-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4301f-134">required</span></span>  <br/> |<span data-ttu-id="4301f-135">Указывает связь с частью.</span><span class="sxs-lookup"><span data-stu-id="4301f-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="4301f-136">«Удалить #»</span><span class="sxs-lookup"><span data-stu-id="4301f-136">"rId#"</span></span>  <br/> <span data-ttu-id="4301f-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="4301f-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4301f-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="4301f-138">Remarks</span></span>

<span data-ttu-id="4301f-139">Значение атрибута **r: id** должен быть указан тип **простом типе ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="4301f-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="4301f-140">Тип **простом типе ST_RelationshipID** — это строка, которая должна быть в формате «избавиться #», где последний символ, должно быть числом.</span><span class="sxs-lookup"><span data-stu-id="4301f-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="4301f-141">Номер должен быть уникальным во все элементы одного уровня элемента **Rel** .</span><span class="sxs-lookup"><span data-stu-id="4301f-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="4301f-142">Дополнительные сведения о типе простом типе ST_RelationshipID можно найти в [спецификации ISO/IEC 29500 часть 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="4301f-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

