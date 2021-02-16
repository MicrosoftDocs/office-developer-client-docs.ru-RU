---
title: Paragraph_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: fd7c5233b89bc92ed449d3d8d2767daa23ea8071
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540597"
---
# <a name="paragraph_type-complextype-visio-xml"></a><span data-ttu-id="f1246-102">Paragraph_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1246-102">Paragraph_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f1246-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f1246-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1246-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f1246-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f1246-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f1246-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f1246-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f1246-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f1246-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f1246-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f1246-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="f1246-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1246-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f1246-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1246-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1246-110">Elements and attributes</span></span>

<span data-ttu-id="f1246-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f1246-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f1246-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f1246-112">Child elements</span></span>

|<span data-ttu-id="f1246-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f1246-113">**Element**</span></span>|<span data-ttu-id="f1246-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1246-114">**Type**</span></span>|<span data-ttu-id="f1246-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1246-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1246-116">Row</span><span class="sxs-lookup"><span data-stu-id="f1246-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f1246-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="f1246-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f1246-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1246-118">Attributes</span></span>

<span data-ttu-id="f1246-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="f1246-119">None.</span></span>
  

