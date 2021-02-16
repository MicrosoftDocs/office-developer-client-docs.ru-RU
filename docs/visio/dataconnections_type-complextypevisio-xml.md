---
title: DataConnections_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542459"
---
# <a name="dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="532f6-102">DataConnections_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="532f6-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="532f6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="532f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="532f6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="532f6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="532f6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="532f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="532f6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="532f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="532f6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="532f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="532f6-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="532f6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="532f6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="532f6-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="532f6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="532f6-110">Elements and attributes</span></span>

<span data-ttu-id="532f6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="532f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="532f6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="532f6-112">Child elements</span></span>

|<span data-ttu-id="532f6-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="532f6-113">**Element**</span></span>|<span data-ttu-id="532f6-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="532f6-114">**Type**</span></span>|<span data-ttu-id="532f6-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="532f6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="532f6-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="532f6-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="532f6-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="532f6-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="532f6-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="532f6-118">Attributes</span></span>

|<span data-ttu-id="532f6-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="532f6-119">**Attribute**</span></span>|<span data-ttu-id="532f6-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="532f6-120">**Type**</span></span>|<span data-ttu-id="532f6-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="532f6-121">**Required**</span></span>|<span data-ttu-id="532f6-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="532f6-122">**Description**</span></span>|<span data-ttu-id="532f6-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="532f6-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="532f6-124">NextID</span><span class="sxs-lookup"><span data-stu-id="532f6-124">NextID</span></span>  <br/> |<span data-ttu-id="532f6-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="532f6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="532f6-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="532f6-126">required</span></span>  <br/> ||<span data-ttu-id="532f6-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="532f6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

