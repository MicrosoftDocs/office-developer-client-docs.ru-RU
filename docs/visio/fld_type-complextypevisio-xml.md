---
title: fld_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390606"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="d960c-102">fld_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d960c-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d960c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d960c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d960c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d960c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d960c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d960c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d960c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d960c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d960c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="d960c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d960c-108">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d960c-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d960c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d960c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d960c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d960c-110">Elements and attributes</span></span>

<span data-ttu-id="d960c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d960c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d960c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d960c-112">Child elements</span></span>

<span data-ttu-id="d960c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="d960c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d960c-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d960c-114">Attributes</span></span>

|<span data-ttu-id="d960c-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d960c-115">**Attribute**</span></span>|<span data-ttu-id="d960c-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d960c-116">**Type**</span></span>|<span data-ttu-id="d960c-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d960c-117">**Required**</span></span>|<span data-ttu-id="d960c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d960c-118">**Description**</span></span>|<span data-ttu-id="d960c-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d960c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d960c-120">IX</span><span class="sxs-lookup"><span data-stu-id="d960c-120">IX</span></span>  <br/> |<span data-ttu-id="d960c-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d960c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d960c-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d960c-122">required</span></span>  <br/> ||<span data-ttu-id="d960c-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d960c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

