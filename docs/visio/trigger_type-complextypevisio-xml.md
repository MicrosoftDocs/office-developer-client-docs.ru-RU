---
title: Trigger_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541899"
---
# <a name="trigger_type-complextype-visio-xml"></a><span data-ttu-id="4efe0-102">Trigger_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4efe0-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4efe0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4efe0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4efe0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4efe0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4efe0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4efe0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4efe0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4efe0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4efe0-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4efe0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4efe0-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4efe0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4efe0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4efe0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4efe0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4efe0-110">Elements and attributes</span></span>

<span data-ttu-id="4efe0-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4efe0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4efe0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4efe0-112">Child elements</span></span>

|<span data-ttu-id="4efe0-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4efe0-113">**Element**</span></span>|<span data-ttu-id="4efe0-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4efe0-114">**Type**</span></span>|<span data-ttu-id="4efe0-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4efe0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4efe0-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="4efe0-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4efe0-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4efe0-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4efe0-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4efe0-118">Attributes</span></span>

|<span data-ttu-id="4efe0-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4efe0-119">**Attribute**</span></span>|<span data-ttu-id="4efe0-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4efe0-120">**Type**</span></span>|<span data-ttu-id="4efe0-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4efe0-121">**Required**</span></span>|<span data-ttu-id="4efe0-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4efe0-122">**Description**</span></span>|<span data-ttu-id="4efe0-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4efe0-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4efe0-124">Нет</span><span class="sxs-lookup"><span data-stu-id="4efe0-124">N</span></span>  <br/> |<span data-ttu-id="4efe0-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4efe0-125">xsd:string</span></span>  <br/> |<span data-ttu-id="4efe0-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4efe0-126">required</span></span>  <br/> ||<span data-ttu-id="4efe0-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4efe0-127">Values of the xsd:string type.</span></span>  <br/> |
   

