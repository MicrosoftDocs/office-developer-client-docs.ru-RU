---
title: fld_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: c4ea016adea237258ba699c54bf05b902119eca1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813781"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="44f02-102">fld_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="44f02-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="44f02-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="44f02-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44f02-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="44f02-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="44f02-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="44f02-105">**Schema file**</span></span> <br/> |<span data-ttu-id="44f02-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="44f02-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="44f02-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="44f02-107">**Extension base**</span></span> <br/> |<span data-ttu-id="44f02-108">XSD:String</span><span class="sxs-lookup"><span data-stu-id="44f02-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44f02-109">Определение</span><span class="sxs-lookup"><span data-stu-id="44f02-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="44f02-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="44f02-110">Elements and attributes</span></span>

<span data-ttu-id="44f02-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="44f02-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="44f02-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="44f02-112">Child elements</span></span>

<span data-ttu-id="44f02-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="44f02-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44f02-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="44f02-114">Attributes</span></span>

|<span data-ttu-id="44f02-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="44f02-115">**Attribute**</span></span>|<span data-ttu-id="44f02-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="44f02-116">**Type**</span></span>|<span data-ttu-id="44f02-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="44f02-117">**Required**</span></span>|<span data-ttu-id="44f02-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="44f02-118">**Description**</span></span>|<span data-ttu-id="44f02-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="44f02-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="44f02-120">IX</span><span class="sxs-lookup"><span data-stu-id="44f02-120">IX</span></span>  <br/> |<span data-ttu-id="44f02-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="44f02-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="44f02-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="44f02-122">required</span></span>  <br/> ||<span data-ttu-id="44f02-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="44f02-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

