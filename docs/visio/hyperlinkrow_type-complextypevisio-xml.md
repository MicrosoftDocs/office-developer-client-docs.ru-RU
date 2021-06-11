---
title: HyperlinkRow_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 64705604ce12f032f49827b28fa3e61e879f2162
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541507"
---
# <a name="hyperlinkrow_type-complextype-visio-xml"></a><span data-ttu-id="f0e98-102">HyperlinkRow_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f0e98-102">HyperlinkRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f0e98-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f0e98-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0e98-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f0e98-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f0e98-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f0e98-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f0e98-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f0e98-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f0e98-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f0e98-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f0e98-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="f0e98-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0e98-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f0e98-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0e98-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0e98-110">Elements and attributes</span></span>

<span data-ttu-id="f0e98-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f0e98-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f0e98-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f0e98-112">Child elements</span></span>

|<span data-ttu-id="f0e98-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f0e98-113">**Element**</span></span>|<span data-ttu-id="f0e98-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f0e98-114">**Type**</span></span>|<span data-ttu-id="f0e98-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0e98-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0e98-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f0e98-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="f0e98-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f0e98-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f0e98-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0e98-118">Attributes</span></span>

<span data-ttu-id="f0e98-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="f0e98-119">None.</span></span>
  

