---
title: Элемент rel (ForeignData_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает связь между фигурой и частью документа, которая содержит данные изображения, связанные с фигурой.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542809"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="128f0-103">Элемент rel (ForeignData_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="128f0-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="128f0-104">Указывает связь между фигурой и частью документа, которая содержит данные изображения, связанные с фигурой.</span><span class="sxs-lookup"><span data-stu-id="128f0-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="128f0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="128f0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="128f0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="128f0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="128f0-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="128f0-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="128f0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="128f0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="128f0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="128f0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="128f0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="128f0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="128f0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="128f0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="128f0-112">Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="128f0-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="128f0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="128f0-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="128f0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="128f0-114">Elements and attributes</span></span>

<span data-ttu-id="128f0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="128f0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="128f0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="128f0-116">Parent elements</span></span>

|<span data-ttu-id="128f0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="128f0-117">**Element**</span></span>|<span data-ttu-id="128f0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="128f0-118">**Type**</span></span>|<span data-ttu-id="128f0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="128f0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="128f0-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="128f0-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="128f0-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="128f0-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="128f0-122">Указывает один экземпляр графических данных, хранящихся в документе.</span><span class="sxs-lookup"><span data-stu-id="128f0-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="128f0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="128f0-123">Child elements</span></span>

<span data-ttu-id="128f0-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="128f0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="128f0-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="128f0-125">Attributes</span></span>

|<span data-ttu-id="128f0-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="128f0-126">**Attribute**</span></span>|<span data-ttu-id="128f0-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="128f0-127">**Type**</span></span>|<span data-ttu-id="128f0-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="128f0-128">**Required**</span></span>|<span data-ttu-id="128f0-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="128f0-129">**Description**</span></span>|<span data-ttu-id="128f0-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="128f0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="128f0-131">р:ид</span><span class="sxs-lookup"><span data-stu-id="128f0-131">r:id</span></span>  <br/> |<span data-ttu-id="128f0-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="128f0-132">xsd:string</span></span>  <br/> <span data-ttu-id="128f0-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="128f0-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="128f0-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="128f0-134">required</span></span>  <br/> |<span data-ttu-id="128f0-135">Задает отношение к части.</span><span class="sxs-lookup"><span data-stu-id="128f0-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="128f0-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="128f0-136">"rId#"</span></span>  <br/> <span data-ttu-id="128f0-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="128f0-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="128f0-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="128f0-138">Remarks</span></span>

<span data-ttu-id="128f0-139">Значение атрибута **р:ИД** должно быть типом **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="128f0-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="128f0-140">Тип **ST_RelationshipID** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом.</span><span class="sxs-lookup"><span data-stu-id="128f0-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="128f0-141">Число должно быть уникальным среди всех родственных элементов элемента **rel** .</span><span class="sxs-lookup"><span data-stu-id="128f0-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="128f0-142">Для получения дополнительных сведений о типе ST_RelationshipID, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="128f0-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

