---
title: RefBy_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 5042a618420a72284e0ef75c5d624c6f5464e162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814528"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="d5481-102">RefBy_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d5481-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d5481-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d5481-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5481-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d5481-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5481-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d5481-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5481-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5481-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5481-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d5481-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5481-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d5481-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5481-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d5481-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5481-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5481-110">Elements and attributes</span></span>

<span data-ttu-id="d5481-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d5481-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5481-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d5481-112">Child elements</span></span>

<span data-ttu-id="d5481-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="d5481-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5481-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5481-114">Attributes</span></span>

|<span data-ttu-id="d5481-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d5481-115">**Attribute**</span></span>|<span data-ttu-id="d5481-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5481-116">**Type**</span></span>|<span data-ttu-id="d5481-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d5481-117">**Required**</span></span>|<span data-ttu-id="d5481-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5481-118">**Description**</span></span>|<span data-ttu-id="d5481-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d5481-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5481-120">ID</span><span class="sxs-lookup"><span data-stu-id="d5481-120">ID</span></span>  <br/> |<span data-ttu-id="d5481-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5481-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5481-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d5481-122">required</span></span>  <br/> ||<span data-ttu-id="d5481-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5481-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5481-124">T</span><span class="sxs-lookup"><span data-stu-id="d5481-124">T</span></span>  <br/> |<span data-ttu-id="d5481-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5481-125">xsd:string</span></span>  <br/> |<span data-ttu-id="d5481-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d5481-126">required</span></span>  <br/> ||<span data-ttu-id="d5481-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5481-127">Values of the xsd:string type.</span></span>  <br/> |
   

