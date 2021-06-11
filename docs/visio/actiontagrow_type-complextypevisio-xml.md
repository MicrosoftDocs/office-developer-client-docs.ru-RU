---
title: ActionTagRow_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 7d2822cb0df0b18e7f19e380fc3e1ba9e4f10c69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541374"
---
# <a name="actiontagrow_type-complextype-visio-xml"></a><span data-ttu-id="43b86-102">ActionTagRow_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="43b86-102">ActionTagRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="43b86-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="43b86-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43b86-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="43b86-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43b86-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="43b86-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43b86-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="43b86-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43b86-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="43b86-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43b86-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="43b86-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43b86-109">Определение</span><span class="sxs-lookup"><span data-stu-id="43b86-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="43b86-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="43b86-110">Elements and attributes</span></span>

<span data-ttu-id="43b86-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="43b86-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43b86-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="43b86-112">Child elements</span></span>

|<span data-ttu-id="43b86-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="43b86-113">**Element**</span></span>|<span data-ttu-id="43b86-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="43b86-114">**Type**</span></span>|<span data-ttu-id="43b86-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43b86-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43b86-116">Cell</span><span class="sxs-lookup"><span data-stu-id="43b86-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="43b86-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="43b86-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="43b86-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43b86-118">Attributes</span></span>

<span data-ttu-id="43b86-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="43b86-119">None.</span></span>
  

