---
title: Тригжер_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280859"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="6b495-102">Тригжер_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6b495-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6b495-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6b495-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b495-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b495-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6b495-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b495-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6b495-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6b495-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6b495-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6b495-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6b495-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="6b495-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b495-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6b495-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b495-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b495-110">Elements and attributes</span></span>

<span data-ttu-id="6b495-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b495-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6b495-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b495-112">Child elements</span></span>

|<span data-ttu-id="6b495-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b495-113">**Element**</span></span>|<span data-ttu-id="6b495-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b495-114">**Type**</span></span>|<span data-ttu-id="6b495-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b495-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b495-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="6b495-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b495-117">Рефби_типе</span><span class="sxs-lookup"><span data-stu-id="6b495-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6b495-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b495-118">Attributes</span></span>

|<span data-ttu-id="6b495-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6b495-119">**Attribute**</span></span>|<span data-ttu-id="6b495-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b495-120">**Type**</span></span>|<span data-ttu-id="6b495-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6b495-121">**Required**</span></span>|<span data-ttu-id="6b495-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b495-122">**Description**</span></span>|<span data-ttu-id="6b495-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6b495-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b495-124">N</span><span class="sxs-lookup"><span data-stu-id="6b495-124">N</span></span>  <br/> |<span data-ttu-id="6b495-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b495-125">xsd:string</span></span>  <br/> |<span data-ttu-id="6b495-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b495-126">required</span></span>  <br/> ||<span data-ttu-id="6b495-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b495-127">Values of the xsd:string type.</span></span>  <br/> |
   

