---
title: ColorEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813394"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="8431c-102">ColorEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="8431c-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8431c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8431c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8431c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8431c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8431c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8431c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8431c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8431c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8431c-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="8431c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8431c-108">Нет</span><span class="sxs-lookup"><span data-stu-id="8431c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8431c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8431c-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8431c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8431c-110">Elements and attributes</span></span>

<span data-ttu-id="8431c-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="8431c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8431c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8431c-112">Child elements</span></span>

<span data-ttu-id="8431c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="8431c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8431c-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8431c-114">Attributes</span></span>

|<span data-ttu-id="8431c-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8431c-115">**Attribute**</span></span>|<span data-ttu-id="8431c-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8431c-116">**Type**</span></span>|<span data-ttu-id="8431c-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="8431c-117">**Required**</span></span>|<span data-ttu-id="8431c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8431c-118">**Description**</span></span>|<span data-ttu-id="8431c-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8431c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8431c-120">IX</span><span class="sxs-lookup"><span data-stu-id="8431c-120">IX</span></span>  <br/> |<span data-ttu-id="8431c-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8431c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8431c-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8431c-122">required</span></span>  <br/> ||<span data-ttu-id="8431c-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8431c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8431c-124">RGB</span><span class="sxs-lookup"><span data-stu-id="8431c-124">RGB</span></span>  <br/> |<span data-ttu-id="8431c-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8431c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="8431c-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8431c-126">required</span></span>  <br/> ||<span data-ttu-id="8431c-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8431c-127">Values of the xsd:string type.</span></span>  <br/> |
   

