---
title: RowKeyValue_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387687"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="92500-102">RowKeyValue_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="92500-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="92500-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="92500-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92500-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="92500-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92500-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="92500-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92500-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="92500-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92500-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="92500-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92500-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="92500-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92500-109">Определение</span><span class="sxs-lookup"><span data-stu-id="92500-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92500-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="92500-110">Elements and attributes</span></span>

<span data-ttu-id="92500-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="92500-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92500-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="92500-112">Child elements</span></span>

<span data-ttu-id="92500-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="92500-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92500-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="92500-114">Attributes</span></span>

|<span data-ttu-id="92500-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="92500-115">**Attribute**</span></span>|<span data-ttu-id="92500-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="92500-116">**Type**</span></span>|<span data-ttu-id="92500-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="92500-117">**Required**</span></span>|<span data-ttu-id="92500-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="92500-118">**Description**</span></span>|<span data-ttu-id="92500-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="92500-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92500-120">RowID</span><span class="sxs-lookup"><span data-stu-id="92500-120">RowID</span></span>  <br/> |<span data-ttu-id="92500-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92500-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92500-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="92500-122">required</span></span>  <br/> ||<span data-ttu-id="92500-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="92500-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92500-124">Значение</span><span class="sxs-lookup"><span data-stu-id="92500-124">Value</span></span>  <br/> |<span data-ttu-id="92500-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="92500-125">xsd:string</span></span>  <br/> |<span data-ttu-id="92500-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="92500-126">required</span></span>  <br/> ||<span data-ttu-id="92500-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="92500-127">Values of the xsd:string type.</span></span>  <br/> |
   

