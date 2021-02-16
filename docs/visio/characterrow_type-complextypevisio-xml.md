---
title: CharacterRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: 3d54921ca571ff3ba4643b2e1d18ee9d7d1bc8c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540198"
---
# <a name="characterrow_type-complextype-visio-xml"></a><span data-ttu-id="47509-102">CharacterRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="47509-102">CharacterRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="47509-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="47509-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47509-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="47509-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47509-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="47509-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47509-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47509-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47509-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="47509-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47509-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="47509-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47509-109">Определение</span><span class="sxs-lookup"><span data-stu-id="47509-109">Definition</span></span>

```XML
          <xs:complexType name="CharacterRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="47509-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="47509-110">Elements and attributes</span></span>

<span data-ttu-id="47509-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="47509-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47509-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="47509-112">Child elements</span></span>

|<span data-ttu-id="47509-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="47509-113">**Element**</span></span>|<span data-ttu-id="47509-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="47509-114">**Type**</span></span>|<span data-ttu-id="47509-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47509-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47509-116">Cell</span><span class="sxs-lookup"><span data-stu-id="47509-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="47509-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="47509-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="47509-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="47509-118">Attributes</span></span>

<span data-ttu-id="47509-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="47509-119">None.</span></span>
  

