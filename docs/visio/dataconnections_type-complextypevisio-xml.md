---
title: DataConnections_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813540"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="0921f-102">DataConnections_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0921f-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0921f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0921f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0921f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0921f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0921f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0921f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0921f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0921f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0921f-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="0921f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0921f-108">Нет</span><span class="sxs-lookup"><span data-stu-id="0921f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0921f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0921f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0921f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0921f-110">Elements and attributes</span></span>

<span data-ttu-id="0921f-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="0921f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0921f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0921f-112">Child elements</span></span>

|<span data-ttu-id="0921f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0921f-113">**Element**</span></span>|<span data-ttu-id="0921f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0921f-114">**Type**</span></span>|<span data-ttu-id="0921f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0921f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0921f-116">Подключение данных</span><span class="sxs-lookup"><span data-stu-id="0921f-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0921f-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="0921f-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0921f-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0921f-118">Attributes</span></span>

|<span data-ttu-id="0921f-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0921f-119">**Attribute**</span></span>|<span data-ttu-id="0921f-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0921f-120">**Type**</span></span>|<span data-ttu-id="0921f-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="0921f-121">**Required**</span></span>|<span data-ttu-id="0921f-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0921f-122">**Description**</span></span>|<span data-ttu-id="0921f-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0921f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0921f-124">NextID</span><span class="sxs-lookup"><span data-stu-id="0921f-124">NextID</span></span>  <br/> |<span data-ttu-id="0921f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0921f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0921f-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0921f-126">required</span></span>  <br/> ||<span data-ttu-id="0921f-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0921f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

