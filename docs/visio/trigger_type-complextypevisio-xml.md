---
title: Trigger_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815062"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="49fe5-102">Trigger_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="49fe5-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="49fe5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="49fe5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49fe5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="49fe5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="49fe5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="49fe5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="49fe5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="49fe5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="49fe5-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="49fe5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="49fe5-108">Нет</span><span class="sxs-lookup"><span data-stu-id="49fe5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="49fe5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="49fe5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="49fe5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="49fe5-110">Elements and attributes</span></span>

<span data-ttu-id="49fe5-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="49fe5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="49fe5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="49fe5-112">Child elements</span></span>

|<span data-ttu-id="49fe5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="49fe5-113">**Element**</span></span>|<span data-ttu-id="49fe5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="49fe5-114">**Type**</span></span>|<span data-ttu-id="49fe5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="49fe5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="49fe5-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="49fe5-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49fe5-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="49fe5-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="49fe5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="49fe5-118">Attributes</span></span>

|<span data-ttu-id="49fe5-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="49fe5-119">**Attribute**</span></span>|<span data-ttu-id="49fe5-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="49fe5-120">**Type**</span></span>|<span data-ttu-id="49fe5-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="49fe5-121">**Required**</span></span>|<span data-ttu-id="49fe5-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="49fe5-122">**Description**</span></span>|<span data-ttu-id="49fe5-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="49fe5-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="49fe5-124">N</span><span class="sxs-lookup"><span data-stu-id="49fe5-124">N</span></span>  <br/> |<span data-ttu-id="49fe5-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="49fe5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="49fe5-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="49fe5-126">required</span></span>  <br/> ||<span data-ttu-id="49fe5-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="49fe5-127">Values of the xsd:string type.</span></span>  <br/> |
   

