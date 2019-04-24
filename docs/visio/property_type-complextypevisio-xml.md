---
title: Проперти_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ada20c601fcd42bf551a0aea63787aac96062816
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326875"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="47b44-102">Проперти_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="47b44-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47b44-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="47b44-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47b44-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="47b44-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47b44-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="47b44-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47b44-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47b44-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47b44-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="47b44-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47b44-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="47b44-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47b44-109">Определение</span><span class="sxs-lookup"><span data-stu-id="47b44-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47b44-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="47b44-110">Elements and attributes</span></span>

<span data-ttu-id="47b44-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="47b44-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47b44-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="47b44-112">Child elements</span></span>

|<span data-ttu-id="47b44-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="47b44-113">**Element**</span></span>|<span data-ttu-id="47b44-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="47b44-114">**Type**</span></span>|<span data-ttu-id="47b44-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47b44-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47b44-116">Row</span><span class="sxs-lookup"><span data-stu-id="47b44-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="47b44-117">Пропертиров_типе</span><span class="sxs-lookup"><span data-stu-id="47b44-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="47b44-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="47b44-118">Attributes</span></span>

<span data-ttu-id="47b44-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="47b44-119">None.</span></span>
  

