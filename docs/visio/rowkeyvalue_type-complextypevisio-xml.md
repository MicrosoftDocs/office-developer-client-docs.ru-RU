---
title: RowKeyValue_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541724"
---
# <a name="rowkeyvalue_type-complextype-visio-xml"></a><span data-ttu-id="56c6e-102">RowKeyValue_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="56c6e-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="56c6e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="56c6e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56c6e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="56c6e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="56c6e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="56c6e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="56c6e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="56c6e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="56c6e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="56c6e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="56c6e-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="56c6e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56c6e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="56c6e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="56c6e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="56c6e-110">Elements and attributes</span></span>

<span data-ttu-id="56c6e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="56c6e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="56c6e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="56c6e-112">Child elements</span></span>

<span data-ttu-id="56c6e-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="56c6e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56c6e-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="56c6e-114">Attributes</span></span>

|<span data-ttu-id="56c6e-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="56c6e-115">**Attribute**</span></span>|<span data-ttu-id="56c6e-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="56c6e-116">**Type**</span></span>|<span data-ttu-id="56c6e-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="56c6e-117">**Required**</span></span>|<span data-ttu-id="56c6e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56c6e-118">**Description**</span></span>|<span data-ttu-id="56c6e-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="56c6e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="56c6e-120">RowID</span><span class="sxs-lookup"><span data-stu-id="56c6e-120">RowID</span></span>  <br/> |<span data-ttu-id="56c6e-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="56c6e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="56c6e-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56c6e-122">required</span></span>  <br/> ||<span data-ttu-id="56c6e-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="56c6e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="56c6e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56c6e-124">Value</span></span>  <br/> |<span data-ttu-id="56c6e-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="56c6e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="56c6e-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56c6e-126">required</span></span>  <br/> ||<span data-ttu-id="56c6e-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="56c6e-127">Values of the xsd:string type.</span></span>  <br/> |
   

