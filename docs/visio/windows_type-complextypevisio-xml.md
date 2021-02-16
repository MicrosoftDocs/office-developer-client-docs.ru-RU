---
title: Windows_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538440"
---
# <a name="windows_type-complextype-visio-xml"></a><span data-ttu-id="6fa0c-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6fa0c-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6fa0c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6fa0c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fa0c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6fa0c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6fa0c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6fa0c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6fa0c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6fa0c-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="6fa0c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6fa0c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6fa0c-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6fa0c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6fa0c-110">Elements and attributes</span></span>

<span data-ttu-id="6fa0c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6fa0c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6fa0c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6fa0c-112">Child elements</span></span>

|<span data-ttu-id="6fa0c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-113">**Element**</span></span>|<span data-ttu-id="6fa0c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-114">**Type**</span></span>|<span data-ttu-id="6fa0c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6fa0c-116">Window</span><span class="sxs-lookup"><span data-stu-id="6fa0c-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fa0c-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="6fa0c-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6fa0c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6fa0c-118">Attributes</span></span>

|<span data-ttu-id="6fa0c-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-119">**Attribute**</span></span>|<span data-ttu-id="6fa0c-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-120">**Type**</span></span>|<span data-ttu-id="6fa0c-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-121">**Required**</span></span>|<span data-ttu-id="6fa0c-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-122">**Description**</span></span>|<span data-ttu-id="6fa0c-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6fa0c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6fa0c-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="6fa0c-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="6fa0c-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6fa0c-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6fa0c-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="6fa0c-126">optional</span></span>  <br/> ||<span data-ttu-id="6fa0c-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6fa0c-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6fa0c-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="6fa0c-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="6fa0c-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6fa0c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6fa0c-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="6fa0c-130">optional</span></span>  <br/> ||<span data-ttu-id="6fa0c-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6fa0c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

