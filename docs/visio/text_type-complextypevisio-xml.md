---
title: Текст_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: cfacc84cb8b38acfbda3c37c669dd9714d899098
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541381"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="1d7f9-102">Текст_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1d7f9-102">Text_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1d7f9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1d7f9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d7f9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1d7f9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1d7f9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1d7f9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1d7f9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1d7f9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1d7f9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d7f9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1d7f9-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d7f9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d7f9-110">Elements and attributes</span></span>

<span data-ttu-id="1d7f9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1d7f9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1d7f9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1d7f9-112">Child elements</span></span>

|<span data-ttu-id="1d7f9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-113">**Element**</span></span>|<span data-ttu-id="1d7f9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-114">**Type**</span></span>|<span data-ttu-id="1d7f9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d7f9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d7f9-116">CP</span><span class="sxs-lookup"><span data-stu-id="1d7f9-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d7f9-117">Кп_типе</span><span class="sxs-lookup"><span data-stu-id="1d7f9-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1d7f9-118">FLD</span><span class="sxs-lookup"><span data-stu-id="1d7f9-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d7f9-119">Флд_типе</span><span class="sxs-lookup"><span data-stu-id="1d7f9-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1d7f9-120">PP</span><span class="sxs-lookup"><span data-stu-id="1d7f9-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d7f9-121">Пп_типе</span><span class="sxs-lookup"><span data-stu-id="1d7f9-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1d7f9-122">Пи</span><span class="sxs-lookup"><span data-stu-id="1d7f9-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d7f9-123">Тп_типе</span><span class="sxs-lookup"><span data-stu-id="1d7f9-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1d7f9-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d7f9-124">Attributes</span></span>

<span data-ttu-id="1d7f9-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="1d7f9-125">None.</span></span>
  

