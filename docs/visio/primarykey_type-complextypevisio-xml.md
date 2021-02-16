---
title: PrimaryKey_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538797"
---
# <a name="primarykey_type-complextype-visio-xml"></a><span data-ttu-id="9570d-102">PrimaryKey_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9570d-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9570d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9570d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9570d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9570d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9570d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9570d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9570d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9570d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9570d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9570d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9570d-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9570d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9570d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9570d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9570d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9570d-110">Elements and attributes</span></span>

<span data-ttu-id="9570d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9570d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9570d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9570d-112">Child elements</span></span>

|<span data-ttu-id="9570d-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9570d-113">**Element**</span></span>|<span data-ttu-id="9570d-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9570d-114">**Type**</span></span>|<span data-ttu-id="9570d-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9570d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9570d-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="9570d-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9570d-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="9570d-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9570d-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9570d-118">Attributes</span></span>

|<span data-ttu-id="9570d-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9570d-119">**Attribute**</span></span>|<span data-ttu-id="9570d-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9570d-120">**Type**</span></span>|<span data-ttu-id="9570d-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9570d-121">**Required**</span></span>|<span data-ttu-id="9570d-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9570d-122">**Description**</span></span>|<span data-ttu-id="9570d-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9570d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9570d-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="9570d-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="9570d-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9570d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9570d-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9570d-126">required</span></span>  <br/> ||<span data-ttu-id="9570d-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9570d-127">Values of the xsd:string type.</span></span>  <br/> |
   

