---
title: PrimaryKey_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814485"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="e0d55-102">PrimaryKey_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e0d55-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e0d55-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e0d55-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0d55-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e0d55-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0d55-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e0d55-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0d55-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0d55-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0d55-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="e0d55-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0d55-108">Нет</span><span class="sxs-lookup"><span data-stu-id="e0d55-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0d55-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e0d55-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0d55-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e0d55-110">Elements and attributes</span></span>

<span data-ttu-id="e0d55-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="e0d55-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0d55-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e0d55-112">Child elements</span></span>

|<span data-ttu-id="e0d55-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e0d55-113">**Element**</span></span>|<span data-ttu-id="e0d55-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e0d55-114">**Type**</span></span>|<span data-ttu-id="e0d55-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e0d55-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0d55-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="e0d55-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0d55-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="e0d55-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0d55-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e0d55-118">Attributes</span></span>

|<span data-ttu-id="e0d55-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e0d55-119">**Attribute**</span></span>|<span data-ttu-id="e0d55-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e0d55-120">**Type**</span></span>|<span data-ttu-id="e0d55-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="e0d55-121">**Required**</span></span>|<span data-ttu-id="e0d55-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e0d55-122">**Description**</span></span>|<span data-ttu-id="e0d55-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e0d55-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0d55-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="e0d55-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e0d55-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e0d55-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e0d55-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e0d55-126">required</span></span>  <br/> ||<span data-ttu-id="e0d55-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e0d55-127">Values of the xsd:string type.</span></span>  <br/> |
   

