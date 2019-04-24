---
title: Филлградиентров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40c88316-4710-b5b4-7be4-e3047474d519
ms.openlocfilehash: 7b2432f564463cd625c64779c6797a20b53b19d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322479"
---
# <a name="fillgradientrowtype-complextype-visio-xml"></a><span data-ttu-id="82ae6-102">Филлградиентров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="82ae6-102">FillGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="82ae6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="82ae6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82ae6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="82ae6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="82ae6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="82ae6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="82ae6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="82ae6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="82ae6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="82ae6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="82ae6-108">Индекседров_типе</span><span class="sxs-lookup"><span data-stu-id="82ae6-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82ae6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="82ae6-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradientRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="82ae6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="82ae6-110">Elements and attributes</span></span>

<span data-ttu-id="82ae6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="82ae6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="82ae6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82ae6-112">Child elements</span></span>

|<span data-ttu-id="82ae6-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="82ae6-113">**Element**</span></span>|<span data-ttu-id="82ae6-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="82ae6-114">**Type**</span></span>|<span data-ttu-id="82ae6-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="82ae6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82ae6-116">Cell</span><span class="sxs-lookup"><span data-stu-id="82ae6-116">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="82ae6-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="82ae6-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="82ae6-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="82ae6-118">Attributes</span></span>

<span data-ttu-id="82ae6-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="82ae6-119">None.</span></span>
  

