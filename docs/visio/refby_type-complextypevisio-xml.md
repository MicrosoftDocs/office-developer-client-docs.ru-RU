---
title: Рефби_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348323"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="04db6-102">Рефби_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="04db6-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04db6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="04db6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04db6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="04db6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04db6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="04db6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04db6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04db6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04db6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="04db6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04db6-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="04db6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04db6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="04db6-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04db6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="04db6-110">Elements and attributes</span></span>

<span data-ttu-id="04db6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="04db6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04db6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="04db6-112">Child elements</span></span>

<span data-ttu-id="04db6-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="04db6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04db6-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="04db6-114">Attributes</span></span>

|<span data-ttu-id="04db6-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="04db6-115">**Attribute**</span></span>|<span data-ttu-id="04db6-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="04db6-116">**Type**</span></span>|<span data-ttu-id="04db6-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="04db6-117">**Required**</span></span>|<span data-ttu-id="04db6-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04db6-118">**Description**</span></span>|<span data-ttu-id="04db6-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="04db6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04db6-120">ИД</span><span class="sxs-lookup"><span data-stu-id="04db6-120">ID</span></span>  <br/> |<span data-ttu-id="04db6-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="04db6-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04db6-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="04db6-122">required</span></span>  <br/> ||<span data-ttu-id="04db6-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="04db6-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04db6-124">Д</span><span class="sxs-lookup"><span data-stu-id="04db6-124">T</span></span>  <br/> |<span data-ttu-id="04db6-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="04db6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="04db6-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="04db6-126">required</span></span>  <br/> ||<span data-ttu-id="04db6-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="04db6-127">Values of the xsd:string type.</span></span>  <br/> |
   

