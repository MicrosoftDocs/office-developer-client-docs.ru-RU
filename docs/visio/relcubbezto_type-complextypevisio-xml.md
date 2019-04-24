---
title: Релкуббезто_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 6ec426ef2c7afd913d904c8ceba938549727c799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319966"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="1db6c-102">Релкуббезто_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1db6c-102">RelCubBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1db6c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1db6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1db6c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1db6c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1db6c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1db6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1db6c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1db6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1db6c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1db6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1db6c-108">Жеометриров_типе</span><span class="sxs-lookup"><span data-stu-id="1db6c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1db6c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1db6c-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1db6c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1db6c-110">Elements and attributes</span></span>

<span data-ttu-id="1db6c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1db6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1db6c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1db6c-112">Child elements</span></span>

|<span data-ttu-id="1db6c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1db6c-113">**Element**</span></span>|<span data-ttu-id="1db6c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1db6c-114">**Type**</span></span>|<span data-ttu-id="1db6c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1db6c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1db6c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1db6c-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1db6c-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="1db6c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1db6c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1db6c-118">Attributes</span></span>

<span data-ttu-id="1db6c-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="1db6c-119">None.</span></span>
  

