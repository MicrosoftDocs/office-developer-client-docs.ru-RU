---
title: ValidationProperties_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: eb1373881b1584b77c6663dd4ec375c50a61efd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815122"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="9541e-102">ValidationProperties_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9541e-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9541e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9541e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9541e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9541e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9541e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9541e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9541e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9541e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9541e-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="9541e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9541e-108">Нет</span><span class="sxs-lookup"><span data-stu-id="9541e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9541e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9541e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9541e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9541e-110">Elements and attributes</span></span>

<span data-ttu-id="9541e-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="9541e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9541e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9541e-112">Child elements</span></span>

<span data-ttu-id="9541e-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9541e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9541e-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9541e-114">Attributes</span></span>

|<span data-ttu-id="9541e-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9541e-115">**Attribute**</span></span>|<span data-ttu-id="9541e-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9541e-116">**Type**</span></span>|<span data-ttu-id="9541e-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="9541e-117">**Required**</span></span>|<span data-ttu-id="9541e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9541e-118">**Description**</span></span>|<span data-ttu-id="9541e-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9541e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9541e-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="9541e-120">LastValidated</span></span>  <br/> |<span data-ttu-id="9541e-121">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="9541e-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9541e-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9541e-122">required</span></span>  <br/> ||<span data-ttu-id="9541e-123">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="9541e-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9541e-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="9541e-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="9541e-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="9541e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9541e-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9541e-126">required</span></span>  <br/> ||<span data-ttu-id="9541e-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9541e-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

