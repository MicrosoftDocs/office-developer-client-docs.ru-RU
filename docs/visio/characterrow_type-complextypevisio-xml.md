---
title: CharacterRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: b96d982798f17aaec12a79b659a0bbf462f566fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813386"
---
# <a name="characterrowtype-complextype-visio-xml"></a><span data-ttu-id="2f3e0-102">CharacterRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2f3e0-102">CharacterRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2f3e0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2f3e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f3e0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f3e0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f3e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2f3e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f3e0-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f3e0-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="2f3e0-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f3e0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2f3e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2f3e0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2f3e0-110">Elements and attributes</span></span>

<span data-ttu-id="2f3e0-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="2f3e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f3e0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2f3e0-112">Child elements</span></span>

|<span data-ttu-id="2f3e0-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-113">**Element**</span></span>|<span data-ttu-id="2f3e0-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-114">**Type**</span></span>|<span data-ttu-id="2f3e0-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2f3e0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f3e0-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2f3e0-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2f3e0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2f3e0-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2f3e0-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2f3e0-118">Attributes</span></span>

<span data-ttu-id="2f3e0-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="2f3e0-119">None.</span></span>
  

