---
title: ValidationProperties_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538517"
---
# <a name="validationproperties_type-complextype-visio-xml"></a><span data-ttu-id="c6c55-102">ValidationProperties_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c6c55-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c6c55-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c6c55-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6c55-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c6c55-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c6c55-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c6c55-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c6c55-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c6c55-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c6c55-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="c6c55-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c6c55-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="c6c55-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6c55-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c6c55-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6c55-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6c55-110">Elements and attributes</span></span>

<span data-ttu-id="c6c55-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c6c55-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c6c55-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c6c55-112">Child elements</span></span>

<span data-ttu-id="c6c55-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="c6c55-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6c55-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6c55-114">Attributes</span></span>

|<span data-ttu-id="c6c55-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c6c55-115">**Attribute**</span></span>|<span data-ttu-id="c6c55-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c6c55-116">**Type**</span></span>|<span data-ttu-id="c6c55-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c6c55-117">**Required**</span></span>|<span data-ttu-id="c6c55-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6c55-118">**Description**</span></span>|<span data-ttu-id="c6c55-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c6c55-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6c55-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="c6c55-120">LastValidated</span></span>  <br/> |<span data-ttu-id="c6c55-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="c6c55-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c6c55-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6c55-122">required</span></span>  <br/> ||<span data-ttu-id="c6c55-123">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="c6c55-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="c6c55-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="c6c55-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="c6c55-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c6c55-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c6c55-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6c55-126">required</span></span>  <br/> ||<span data-ttu-id="c6c55-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c6c55-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

