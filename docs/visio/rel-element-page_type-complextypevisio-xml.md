---
title: Элемент rel (Page_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Задает отношение к части с соответствующим XML-документом страницы.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542781"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a><span data-ttu-id="0d5cb-103">Элемент rel (Page_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0d5cb-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0d5cb-104">Задает отношение к части с соответствующим XML-документом страницы.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d5cb-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0d5cb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d5cb-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0d5cb-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="0d5cb-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0d5cb-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0d5cb-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0d5cb-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0d5cb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0d5cb-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0d5cb-112">Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="0d5cb-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d5cb-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0d5cb-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d5cb-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0d5cb-114">Elements and attributes</span></span>

<span data-ttu-id="0d5cb-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0d5cb-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0d5cb-116">Parent elements</span></span>

|<span data-ttu-id="0d5cb-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-117">**Element**</span></span>|<span data-ttu-id="0d5cb-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-118">**Type**</span></span>|<span data-ttu-id="0d5cb-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d5cb-120">Page</span><span class="sxs-lookup"><span data-stu-id="0d5cb-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d5cb-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="0d5cb-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d5cb-122">Задает один экземпляр XML-файла страницы, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d5cb-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0d5cb-123">Child elements</span></span>

<span data-ttu-id="0d5cb-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d5cb-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0d5cb-125">Attributes</span></span>

|<span data-ttu-id="0d5cb-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-126">**Attribute**</span></span>|<span data-ttu-id="0d5cb-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-127">**Type**</span></span>|<span data-ttu-id="0d5cb-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-128">**Required**</span></span>|<span data-ttu-id="0d5cb-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-129">**Description**</span></span>|<span data-ttu-id="0d5cb-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0d5cb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d5cb-131">р:ид</span><span class="sxs-lookup"><span data-stu-id="0d5cb-131">r:id</span></span>  <br/> |<span data-ttu-id="0d5cb-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d5cb-132">xsd:string</span></span>  <br/> <span data-ttu-id="0d5cb-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="0d5cb-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="0d5cb-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0d5cb-134">required</span></span>  <br/> |<span data-ttu-id="0d5cb-135">Задает отношение к части.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="0d5cb-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="0d5cb-136">"rId#"</span></span>  <br/> <span data-ttu-id="0d5cb-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="0d5cb-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d5cb-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d5cb-138">Remarks</span></span>

<span data-ttu-id="0d5cb-139">Значение атрибута **р:ИД** должно быть типом **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="0d5cb-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="0d5cb-140">Тип **ST_RelationshipID** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="0d5cb-141">Число должно быть уникальным среди всех родственных элементов элемента **rel** .</span><span class="sxs-lookup"><span data-stu-id="0d5cb-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="0d5cb-142">Для получения дополнительных сведений о типе ST_RelationshipID, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="0d5cb-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

