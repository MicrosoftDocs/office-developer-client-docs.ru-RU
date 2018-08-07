---
title: ConnectionRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 14a92d20-78fb-0043-7360-7dfda52fb9c7
ms.openlocfilehash: b6fc7b8d3fc62ca4a3659ac55d5e2631ba122f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813481"
---
# <a name="connectionrowtype-complextype-visio-xml"></a><span data-ttu-id="9e4b4-102">ConnectionRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9e4b4-102">ConnectionRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9e4b4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9e4b4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e4b4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9e4b4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9e4b4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9e4b4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9e4b4-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9e4b4-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="9e4b4-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9e4b4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9e4b4-109">Definition</span></span>

```XML
          <xs:complexType name="ConnectionRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="9e4b4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9e4b4-110">Elements and attributes</span></span>

<span data-ttu-id="9e4b4-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="9e4b4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9e4b4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9e4b4-112">Child elements</span></span>

|<span data-ttu-id="9e4b4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-113">**Element**</span></span>|<span data-ttu-id="9e4b4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-114">**Type**</span></span>|<span data-ttu-id="9e4b4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9e4b4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9e4b4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="9e4b4-116">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="9e4b4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9e4b4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9e4b4-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9e4b4-118">Attributes</span></span>

<span data-ttu-id="9e4b4-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="9e4b4-119">None.</span></span>
  

