---
title: Windows_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386560"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="955d4-102">Windows_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="955d4-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="955d4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="955d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="955d4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="955d4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="955d4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="955d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="955d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="955d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="955d4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="955d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="955d4-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="955d4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="955d4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="955d4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="955d4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="955d4-110">Elements and attributes</span></span>

<span data-ttu-id="955d4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="955d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="955d4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="955d4-112">Child elements</span></span>

|<span data-ttu-id="955d4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="955d4-113">**Element**</span></span>|<span data-ttu-id="955d4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="955d4-114">**Type**</span></span>|<span data-ttu-id="955d4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="955d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="955d4-116">Window</span><span class="sxs-lookup"><span data-stu-id="955d4-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="955d4-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="955d4-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="955d4-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="955d4-118">Attributes</span></span>

|<span data-ttu-id="955d4-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="955d4-119">**Attribute**</span></span>|<span data-ttu-id="955d4-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="955d4-120">**Type**</span></span>|<span data-ttu-id="955d4-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="955d4-121">**Required**</span></span>|<span data-ttu-id="955d4-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="955d4-122">**Description**</span></span>|<span data-ttu-id="955d4-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="955d4-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="955d4-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="955d4-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="955d4-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="955d4-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="955d4-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="955d4-126">optional</span></span>  <br/> ||<span data-ttu-id="955d4-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="955d4-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="955d4-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="955d4-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="955d4-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="955d4-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="955d4-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="955d4-130">optional</span></span>  <br/> ||<span data-ttu-id="955d4-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="955d4-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

