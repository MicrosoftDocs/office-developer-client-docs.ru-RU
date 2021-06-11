---
title: fld_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539602"
---
# <a name="fld_type-complextype-visio-xml"></a><span data-ttu-id="f3272-102">fld_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f3272-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f3272-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f3272-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3272-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f3272-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f3272-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f3272-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f3272-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f3272-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f3272-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f3272-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f3272-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f3272-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3272-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f3272-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3272-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f3272-110">Elements and attributes</span></span>

<span data-ttu-id="f3272-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f3272-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f3272-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f3272-112">Child elements</span></span>

<span data-ttu-id="f3272-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f3272-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3272-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f3272-114">Attributes</span></span>

|<span data-ttu-id="f3272-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f3272-115">**Attribute**</span></span>|<span data-ttu-id="f3272-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f3272-116">**Type**</span></span>|<span data-ttu-id="f3272-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f3272-117">**Required**</span></span>|<span data-ttu-id="f3272-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3272-118">**Description**</span></span>|<span data-ttu-id="f3272-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f3272-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3272-120">IX</span><span class="sxs-lookup"><span data-stu-id="f3272-120">IX</span></span>  <br/> |<span data-ttu-id="f3272-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3272-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3272-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f3272-122">required</span></span>  <br/> ||<span data-ttu-id="f3272-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3272-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

