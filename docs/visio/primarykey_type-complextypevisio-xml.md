---
title: Примарикэй_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355988"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="0cd45-102">Примарикэй_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0cd45-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0cd45-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0cd45-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cd45-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0cd45-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0cd45-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0cd45-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0cd45-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0cd45-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0cd45-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0cd45-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0cd45-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0cd45-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0cd45-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd45-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0cd45-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0cd45-110">Elements and attributes</span></span>

<span data-ttu-id="0cd45-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0cd45-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0cd45-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0cd45-112">Child elements</span></span>

|<span data-ttu-id="0cd45-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0cd45-113">**Element**</span></span>|<span data-ttu-id="0cd45-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0cd45-114">**Type**</span></span>|<span data-ttu-id="0cd45-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cd45-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0cd45-116">Ровкэйвалуе</span><span class="sxs-lookup"><span data-stu-id="0cd45-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0cd45-117">Ровкэйвалуе_типе</span><span class="sxs-lookup"><span data-stu-id="0cd45-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0cd45-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0cd45-118">Attributes</span></span>

|<span data-ttu-id="0cd45-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0cd45-119">**Attribute**</span></span>|<span data-ttu-id="0cd45-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0cd45-120">**Type**</span></span>|<span data-ttu-id="0cd45-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0cd45-121">**Required**</span></span>|<span data-ttu-id="0cd45-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cd45-122">**Description**</span></span>|<span data-ttu-id="0cd45-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0cd45-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0cd45-124">Колумннамеид</span><span class="sxs-lookup"><span data-stu-id="0cd45-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="0cd45-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0cd45-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0cd45-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0cd45-126">required</span></span>  <br/> ||<span data-ttu-id="0cd45-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0cd45-127">Values of the xsd:string type.</span></span>  <br/> |
   

