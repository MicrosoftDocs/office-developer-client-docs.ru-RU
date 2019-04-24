---
title: Мовето_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: f3c3ba2bfc789661f57c3d21634b5c876bc11f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283746"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="5e3d4-102">Мовето_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5e3d4-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5e3d4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5e3d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e3d4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5e3d4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5e3d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5e3d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5e3d4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5e3d4-108">Жеометриров_типе</span><span class="sxs-lookup"><span data-stu-id="5e3d4-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e3d4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="5e3d4-109">Definition</span></span>

```XML
          <xs:complexType name="MoveTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5e3d4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5e3d4-110">Elements and attributes</span></span>

<span data-ttu-id="5e3d4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5e3d4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5e3d4-112">Child elements</span></span>

|<span data-ttu-id="5e3d4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-113">**Element**</span></span>|<span data-ttu-id="5e3d4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-114">**Type**</span></span>|<span data-ttu-id="5e3d4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5e3d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e3d4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5e3d4-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="5e3d4-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="5e3d4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5e3d4-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5e3d4-118">Attributes</span></span>

<span data-ttu-id="5e3d4-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-119">None.</span></span>
  

