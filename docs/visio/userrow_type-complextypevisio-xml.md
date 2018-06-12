---
title: UserRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 0d670ecdc9230843cffb0336f3f4ad5c53285615
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815127"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="bda32-102">UserRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bda32-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bda32-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bda32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bda32-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bda32-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bda32-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bda32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bda32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bda32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bda32-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="bda32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bda32-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="bda32-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bda32-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bda32-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="bda32-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bda32-110">Elements and attributes</span></span>

<span data-ttu-id="bda32-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bda32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bda32-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bda32-112">Child elements</span></span>

|<span data-ttu-id="bda32-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bda32-113">**Element**</span></span>|<span data-ttu-id="bda32-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bda32-114">**Type**</span></span>|<span data-ttu-id="bda32-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bda32-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bda32-116">Cell</span><span class="sxs-lookup"><span data-stu-id="bda32-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bda32-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bda32-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bda32-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bda32-118">Attributes</span></span>

<span data-ttu-id="bda32-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="bda32-119">None.</span></span>
  

