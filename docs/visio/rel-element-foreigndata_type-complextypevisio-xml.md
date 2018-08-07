---
title: Элемент Rel (ForeignData_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.
ms.openlocfilehash: f54cd76788d6f5d916b9ed181f309687109dd589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814559"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="66f58-103">Элемент Rel (ForeignData_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="66f58-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="66f58-104">Указывает отношение между фигурой и части документа, который содержит данные изображения, связанного с формой.</span><span class="sxs-lookup"><span data-stu-id="66f58-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66f58-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66f58-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66f58-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="66f58-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66f58-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="66f58-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66f58-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="66f58-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66f58-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="66f58-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66f58-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66f58-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66f58-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="66f58-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66f58-112">Pages.XML, masters.xml, recordsets.xml, страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="66f58-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66f58-113">Определение</span><span class="sxs-lookup"><span data-stu-id="66f58-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66f58-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="66f58-114">Elements and attributes</span></span>

<span data-ttu-id="66f58-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="66f58-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66f58-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="66f58-116">Parent elements</span></span>

|<span data-ttu-id="66f58-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="66f58-117">**Element**</span></span>|<span data-ttu-id="66f58-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="66f58-118">**Type**</span></span>|<span data-ttu-id="66f58-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66f58-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66f58-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="66f58-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66f58-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="66f58-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66f58-122">Один экземпляр данных изображения, хранящиеся в документе.</span><span class="sxs-lookup"><span data-stu-id="66f58-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66f58-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="66f58-123">Child elements</span></span>

<span data-ttu-id="66f58-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="66f58-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66f58-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="66f58-125">Attributes</span></span>

|<span data-ttu-id="66f58-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="66f58-126">**Attribute**</span></span>|<span data-ttu-id="66f58-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="66f58-127">**Type**</span></span>|<span data-ttu-id="66f58-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="66f58-128">**Required**</span></span>|<span data-ttu-id="66f58-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66f58-129">**Description**</span></span>|<span data-ttu-id="66f58-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="66f58-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66f58-131">r: код</span><span class="sxs-lookup"><span data-stu-id="66f58-131">r:id</span></span>  <br/> |<span data-ttu-id="66f58-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="66f58-132">xsd:string</span></span>  <br/> <span data-ttu-id="66f58-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="66f58-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="66f58-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="66f58-134">required</span></span>  <br/> |<span data-ttu-id="66f58-135">Указывает связь с частью.</span><span class="sxs-lookup"><span data-stu-id="66f58-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="66f58-136">«Удалить #»</span><span class="sxs-lookup"><span data-stu-id="66f58-136">"rId#"</span></span>  <br/> <span data-ttu-id="66f58-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="66f58-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66f58-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="66f58-138">Remarks</span></span>

<span data-ttu-id="66f58-139">Значение атрибута **r: id** должен быть указан тип **простом типе ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="66f58-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="66f58-140">Тип **простом типе ST_RelationshipID** — это строка, которая должна быть в формате «избавиться #», где последний символ, должно быть числом.</span><span class="sxs-lookup"><span data-stu-id="66f58-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="66f58-141">Номер должен быть уникальным во все элементы одного уровня элемента **Rel** .</span><span class="sxs-lookup"><span data-stu-id="66f58-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="66f58-142">Дополнительные сведения о типе простом типе ST_RelationshipID можно найти в [спецификации ISO/IEC 29500 часть 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="66f58-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

