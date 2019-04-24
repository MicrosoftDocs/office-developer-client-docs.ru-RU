---
title: Чарактерров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: 40c67d638776015b7aca0992191af154a9852f26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341876"
---
# <a name="characterrowtype-complextype-visio-xml"></a><span data-ttu-id="18249-102">Чарактерров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="18249-102">CharacterRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="18249-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="18249-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18249-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="18249-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="18249-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="18249-105">**Schema file**</span></span> <br/> |<span data-ttu-id="18249-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="18249-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="18249-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="18249-107">**Extension base**</span></span> <br/> |<span data-ttu-id="18249-108">Индекседров_типе</span><span class="sxs-lookup"><span data-stu-id="18249-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18249-109">Определение</span><span class="sxs-lookup"><span data-stu-id="18249-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="18249-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="18249-110">Elements and attributes</span></span>

<span data-ttu-id="18249-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="18249-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="18249-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="18249-112">Child elements</span></span>

|<span data-ttu-id="18249-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="18249-113">**Element**</span></span>|<span data-ttu-id="18249-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="18249-114">**Type**</span></span>|<span data-ttu-id="18249-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18249-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18249-116">Cell</span><span class="sxs-lookup"><span data-stu-id="18249-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="18249-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="18249-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="18249-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18249-118">Attributes</span></span>

<span data-ttu-id="18249-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="18249-119">None.</span></span>
  

