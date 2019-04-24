---
title: Аутолинккомпарисон_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338600"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="f1111-102">Аутолинккомпарисон_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f1111-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f1111-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f1111-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1111-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f1111-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f1111-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f1111-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f1111-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f1111-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f1111-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f1111-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f1111-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f1111-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1111-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f1111-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1111-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1111-110">Elements and attributes</span></span>

<span data-ttu-id="f1111-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f1111-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f1111-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f1111-112">Child elements</span></span>

<span data-ttu-id="f1111-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f1111-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1111-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1111-114">Attributes</span></span>

|<span data-ttu-id="f1111-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f1111-115">**Attribute**</span></span>|<span data-ttu-id="f1111-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1111-116">**Type**</span></span>|<span data-ttu-id="f1111-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f1111-117">**Required**</span></span>|<span data-ttu-id="f1111-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1111-118">**Description**</span></span>|<span data-ttu-id="f1111-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f1111-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1111-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f1111-120">ColumnName</span></span>  <br/> |<span data-ttu-id="f1111-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f1111-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f1111-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1111-122">required</span></span>  <br/> ||<span data-ttu-id="f1111-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f1111-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f1111-124">Контексттипе</span><span class="sxs-lookup"><span data-stu-id="f1111-124">ContextType</span></span>  <br/> |<span data-ttu-id="f1111-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f1111-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f1111-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1111-126">required</span></span>  <br/> ||<span data-ttu-id="f1111-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f1111-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f1111-128">Контексттипелабел</span><span class="sxs-lookup"><span data-stu-id="f1111-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="f1111-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f1111-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f1111-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="f1111-130">optional</span></span>  <br/> ||<span data-ttu-id="f1111-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f1111-131">Values of the xsd:string type.</span></span>  <br/> |
   

