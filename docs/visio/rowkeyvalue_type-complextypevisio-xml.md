---
title: Ровкэйвалуе_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332475"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="603b6-102">Ровкэйвалуе_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="603b6-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="603b6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="603b6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="603b6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="603b6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="603b6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="603b6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="603b6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="603b6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="603b6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="603b6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="603b6-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="603b6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="603b6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="603b6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="603b6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="603b6-110">Elements and attributes</span></span>

<span data-ttu-id="603b6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="603b6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="603b6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="603b6-112">Child elements</span></span>

<span data-ttu-id="603b6-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="603b6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="603b6-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="603b6-114">Attributes</span></span>

|<span data-ttu-id="603b6-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="603b6-115">**Attribute**</span></span>|<span data-ttu-id="603b6-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="603b6-116">**Type**</span></span>|<span data-ttu-id="603b6-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="603b6-117">**Required**</span></span>|<span data-ttu-id="603b6-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="603b6-118">**Description**</span></span>|<span data-ttu-id="603b6-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="603b6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="603b6-120">RowID</span><span class="sxs-lookup"><span data-stu-id="603b6-120">RowID</span></span>  <br/> |<span data-ttu-id="603b6-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="603b6-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="603b6-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="603b6-122">required</span></span>  <br/> ||<span data-ttu-id="603b6-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="603b6-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="603b6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="603b6-124">Value</span></span>  <br/> |<span data-ttu-id="603b6-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="603b6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="603b6-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="603b6-126">required</span></span>  <br/> ||<span data-ttu-id="603b6-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="603b6-127">Values of the xsd:string type.</span></span>  <br/> |
   

