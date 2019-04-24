---
title: Стилешит_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329827"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="f66fb-102">Стилешит_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f66fb-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f66fb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f66fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f66fb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f66fb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f66fb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f66fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f66fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f66fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f66fb-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f66fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f66fb-108">Шит_типе</span><span class="sxs-lookup"><span data-stu-id="f66fb-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f66fb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f66fb-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f66fb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f66fb-110">Elements and attributes</span></span>

<span data-ttu-id="f66fb-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f66fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f66fb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f66fb-112">Child elements</span></span>

<span data-ttu-id="f66fb-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f66fb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f66fb-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f66fb-114">Attributes</span></span>

|<span data-ttu-id="f66fb-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f66fb-115">**Attribute**</span></span>|<span data-ttu-id="f66fb-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f66fb-116">**Type**</span></span>|<span data-ttu-id="f66fb-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f66fb-117">**Required**</span></span>|<span data-ttu-id="f66fb-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f66fb-118">**Description**</span></span>|<span data-ttu-id="f66fb-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f66fb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f66fb-120">ИД</span><span class="sxs-lookup"><span data-stu-id="f66fb-120">ID</span></span>  <br/> |<span data-ttu-id="f66fb-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f66fb-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f66fb-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f66fb-122">required</span></span>  <br/> ||<span data-ttu-id="f66fb-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f66fb-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f66fb-124">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="f66fb-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="f66fb-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f66fb-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f66fb-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="f66fb-126">optional</span></span>  <br/> ||<span data-ttu-id="f66fb-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f66fb-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f66fb-128">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="f66fb-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f66fb-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f66fb-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f66fb-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="f66fb-130">optional</span></span>  <br/> ||<span data-ttu-id="f66fb-131">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f66fb-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f66fb-132">Имя</span><span class="sxs-lookup"><span data-stu-id="f66fb-132">Name</span></span>  <br/> |<span data-ttu-id="f66fb-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f66fb-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f66fb-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="f66fb-134">optional</span></span>  <br/> ||<span data-ttu-id="f66fb-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f66fb-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f66fb-136">NameU</span><span class="sxs-lookup"><span data-stu-id="f66fb-136">NameU</span></span>  <br/> |<span data-ttu-id="f66fb-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f66fb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f66fb-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f66fb-138">optional</span></span>  <br/> ||<span data-ttu-id="f66fb-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f66fb-139">Values of the xsd:string type.</span></span>  <br/> |
   

