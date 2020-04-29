---
title: Элемент rel (Master_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Задает связь с частью с соответствующим главным XML-документом.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542802"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a><span data-ttu-id="f6ad4-103">Элемент rel (Master_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="f6ad4-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f6ad4-104">Задает связь с частью с соответствующим главным XML-документом.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6ad4-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f6ad4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6ad4-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f6ad4-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f6ad4-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6ad4-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6ad4-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f6ad4-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f6ad4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6ad4-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f6ad4-112">Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="f6ad4-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f6ad4-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f6ad4-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6ad4-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f6ad4-114">Elements and attributes</span></span>

<span data-ttu-id="f6ad4-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6ad4-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f6ad4-116">Parent elements</span></span>

|<span data-ttu-id="f6ad4-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-117">**Element**</span></span>|<span data-ttu-id="f6ad4-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-118">**Type**</span></span>|<span data-ttu-id="f6ad4-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6ad4-120">Master</span><span class="sxs-lookup"><span data-stu-id="f6ad4-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f6ad4-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="f6ad4-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6ad4-122">Указывает один экземпляр главного XML-файла, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6ad4-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f6ad4-123">Child elements</span></span>

<span data-ttu-id="f6ad4-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6ad4-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f6ad4-125">Attributes</span></span>

|<span data-ttu-id="f6ad4-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-126">**Attribute**</span></span>|<span data-ttu-id="f6ad4-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-127">**Type**</span></span>|<span data-ttu-id="f6ad4-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-128">**Required**</span></span>|<span data-ttu-id="f6ad4-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-129">**Description**</span></span>|<span data-ttu-id="f6ad4-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f6ad4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6ad4-131">р:ид</span><span class="sxs-lookup"><span data-stu-id="f6ad4-131">r:id</span></span>  <br/> |<span data-ttu-id="f6ad4-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f6ad4-132">xsd:string</span></span>  <br/> <span data-ttu-id="f6ad4-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="f6ad4-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f6ad4-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f6ad4-134">required</span></span>  <br/> |<span data-ttu-id="f6ad4-135">Задает отношение к части.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f6ad4-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="f6ad4-136">"rId#"</span></span>  <br/> <span data-ttu-id="f6ad4-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="f6ad4-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6ad4-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6ad4-138">Remarks</span></span>

<span data-ttu-id="f6ad4-139">Значение атрибута **р:ИД** должно быть типом **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="f6ad4-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f6ad4-140">Тип **ST_RelationshipID** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом.</span><span class="sxs-lookup"><span data-stu-id="f6ad4-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f6ad4-141">Число должно быть уникальным среди всех родственных элементов элемента **rel** .</span><span class="sxs-lookup"><span data-stu-id="f6ad4-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f6ad4-142">Для получения дополнительных сведений о типе ST_RelationshipID, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="f6ad4-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

