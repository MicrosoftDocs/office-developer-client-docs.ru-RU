---
title: LineGradient_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 6be5575336b3fb3ae014abd2685733ce4889f841
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541171"
---
# <a name="linegradient_type-complextype-visio-xml"></a><span data-ttu-id="36313-102">LineGradient_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="36313-102">LineGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="36313-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="36313-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36313-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="36313-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36313-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="36313-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36313-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36313-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36313-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="36313-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36313-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="36313-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36313-109">Определение</span><span class="sxs-lookup"><span data-stu-id="36313-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="36313-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="36313-110">Elements and attributes</span></span>

<span data-ttu-id="36313-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="36313-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36313-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36313-112">Child elements</span></span>

|<span data-ttu-id="36313-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="36313-113">**Element**</span></span>|<span data-ttu-id="36313-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="36313-114">**Type**</span></span>|<span data-ttu-id="36313-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36313-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36313-116">Row</span><span class="sxs-lookup"><span data-stu-id="36313-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="36313-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="36313-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36313-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36313-118">Attributes</span></span>

<span data-ttu-id="36313-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="36313-119">None.</span></span>
  

