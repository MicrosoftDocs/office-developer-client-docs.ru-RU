---
title: RowKeyValue_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: dcd4c972aac1e86fa7a66766a756ebef2cca7c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814679"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="80ab5-102">RowKeyValue_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="80ab5-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="80ab5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="80ab5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80ab5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="80ab5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="80ab5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="80ab5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="80ab5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="80ab5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="80ab5-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="80ab5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="80ab5-108">Нет</span><span class="sxs-lookup"><span data-stu-id="80ab5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80ab5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="80ab5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="80ab5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="80ab5-110">Elements and attributes</span></span>

<span data-ttu-id="80ab5-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="80ab5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="80ab5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="80ab5-112">Child elements</span></span>

<span data-ttu-id="80ab5-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="80ab5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80ab5-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="80ab5-114">Attributes</span></span>

|<span data-ttu-id="80ab5-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="80ab5-115">**Attribute**</span></span>|<span data-ttu-id="80ab5-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="80ab5-116">**Type**</span></span>|<span data-ttu-id="80ab5-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="80ab5-117">**Required**</span></span>|<span data-ttu-id="80ab5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="80ab5-118">**Description**</span></span>|<span data-ttu-id="80ab5-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="80ab5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80ab5-120">RowID</span><span class="sxs-lookup"><span data-stu-id="80ab5-120">RowID</span></span>  <br/> |<span data-ttu-id="80ab5-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80ab5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80ab5-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80ab5-122">required</span></span>  <br/> ||<span data-ttu-id="80ab5-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="80ab5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="80ab5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="80ab5-124">Value</span></span>  <br/> |<span data-ttu-id="80ab5-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="80ab5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="80ab5-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80ab5-126">required</span></span>  <br/> ||<span data-ttu-id="80ab5-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="80ab5-127">Values of the xsd:string type.</span></span>  <br/> |
   

