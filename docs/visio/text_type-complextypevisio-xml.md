---
title: Текст_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332307"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="a5e8f-102">Текст_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a5e8f-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a5e8f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a5e8f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5e8f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a5e8f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a5e8f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a5e8f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a5e8f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a5e8f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a5e8f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5e8f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a5e8f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a5e8f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a5e8f-110">Elements and attributes</span></span>

<span data-ttu-id="a5e8f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a5e8f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a5e8f-112">Child elements</span></span>

|<span data-ttu-id="a5e8f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-113">**Element**</span></span>|<span data-ttu-id="a5e8f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-114">**Type**</span></span>|<span data-ttu-id="a5e8f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a5e8f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5e8f-116">CP</span><span class="sxs-lookup"><span data-stu-id="a5e8f-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5e8f-117">Кп_типе</span><span class="sxs-lookup"><span data-stu-id="a5e8f-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a5e8f-118">FLD</span><span class="sxs-lookup"><span data-stu-id="a5e8f-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5e8f-119">Флд_типе</span><span class="sxs-lookup"><span data-stu-id="a5e8f-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a5e8f-120">PP</span><span class="sxs-lookup"><span data-stu-id="a5e8f-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5e8f-121">Пп_типе</span><span class="sxs-lookup"><span data-stu-id="a5e8f-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a5e8f-122">Пи</span><span class="sxs-lookup"><span data-stu-id="a5e8f-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5e8f-123">Тп_типе</span><span class="sxs-lookup"><span data-stu-id="a5e8f-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a5e8f-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a5e8f-124">Attributes</span></span>

<span data-ttu-id="a5e8f-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-125">None.</span></span>
  

