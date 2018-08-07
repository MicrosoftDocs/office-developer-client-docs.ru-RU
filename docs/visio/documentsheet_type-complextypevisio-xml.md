---
title: DocumentSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813640"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="58305-102">DocumentSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="58305-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="58305-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="58305-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58305-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="58305-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="58305-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="58305-105">**Schema file**</span></span> <br/> |<span data-ttu-id="58305-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="58305-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="58305-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="58305-107">**Extension base**</span></span> <br/> |<span data-ttu-id="58305-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="58305-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58305-109">Определение</span><span class="sxs-lookup"><span data-stu-id="58305-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58305-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="58305-110">Elements and attributes</span></span>

<span data-ttu-id="58305-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="58305-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="58305-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="58305-112">Child elements</span></span>

<span data-ttu-id="58305-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="58305-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58305-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="58305-114">Attributes</span></span>

|<span data-ttu-id="58305-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="58305-115">**Attribute**</span></span>|<span data-ttu-id="58305-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58305-116">**Type**</span></span>|<span data-ttu-id="58305-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="58305-117">**Required**</span></span>|<span data-ttu-id="58305-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58305-118">**Description**</span></span>|<span data-ttu-id="58305-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="58305-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58305-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="58305-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="58305-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="58305-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58305-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="58305-122">optional</span></span>  <br/> ||<span data-ttu-id="58305-123">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="58305-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58305-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="58305-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="58305-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="58305-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58305-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="58305-126">optional</span></span>  <br/> ||<span data-ttu-id="58305-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="58305-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58305-128">Имя</span><span class="sxs-lookup"><span data-stu-id="58305-128">Name</span></span>  <br/> |<span data-ttu-id="58305-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="58305-129">xsd:string</span></span>  <br/> |<span data-ttu-id="58305-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="58305-130">optional</span></span>  <br/> ||<span data-ttu-id="58305-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="58305-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58305-132">NameU</span><span class="sxs-lookup"><span data-stu-id="58305-132">NameU</span></span>  <br/> |<span data-ttu-id="58305-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="58305-133">xsd:string</span></span>  <br/> |<span data-ttu-id="58305-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="58305-134">optional</span></span>  <br/> ||<span data-ttu-id="58305-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="58305-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58305-136">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="58305-136">UniqueID</span></span>  <br/> |<span data-ttu-id="58305-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="58305-137">xsd:string</span></span>  <br/> |<span data-ttu-id="58305-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="58305-138">optional</span></span>  <br/> ||<span data-ttu-id="58305-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="58305-139">Values of the xsd:string type.</span></span>  <br/> |
   

