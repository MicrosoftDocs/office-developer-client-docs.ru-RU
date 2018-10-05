---
title: AutoLinkComparison_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389752"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="41842-102">AutoLinkComparison_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="41842-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="41842-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="41842-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41842-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="41842-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="41842-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="41842-105">**Schema file**</span></span> <br/> |<span data-ttu-id="41842-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="41842-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="41842-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="41842-107">**Extension base**</span></span> <br/> |<span data-ttu-id="41842-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="41842-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41842-109">Определение</span><span class="sxs-lookup"><span data-stu-id="41842-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="41842-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="41842-110">Elements and attributes</span></span>

<span data-ttu-id="41842-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="41842-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41842-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="41842-112">Child elements</span></span>

<span data-ttu-id="41842-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="41842-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41842-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="41842-114">Attributes</span></span>

|<span data-ttu-id="41842-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="41842-115">**Attribute**</span></span>|<span data-ttu-id="41842-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="41842-116">**Type**</span></span>|<span data-ttu-id="41842-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="41842-117">**Required**</span></span>|<span data-ttu-id="41842-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="41842-118">**Description**</span></span>|<span data-ttu-id="41842-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="41842-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41842-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="41842-120">ColumnName</span></span>  <br/> |<span data-ttu-id="41842-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="41842-121">xsd:string</span></span>  <br/> |<span data-ttu-id="41842-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="41842-122">required</span></span>  <br/> ||<span data-ttu-id="41842-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="41842-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="41842-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="41842-124">ContextType</span></span>  <br/> |<span data-ttu-id="41842-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="41842-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="41842-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="41842-126">required</span></span>  <br/> ||<span data-ttu-id="41842-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="41842-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="41842-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="41842-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="41842-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="41842-129">xsd:string</span></span>  <br/> |<span data-ttu-id="41842-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="41842-130">optional</span></span>  <br/> ||<span data-ttu-id="41842-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="41842-131">Values of the xsd:string type.</span></span>  <br/> |
   

