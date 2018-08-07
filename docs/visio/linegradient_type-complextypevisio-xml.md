---
title: LineGradient_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 026527ffb6b74ced088bc22ee715be9df1320334
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814065"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="7dc42-102">LineGradient_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7dc42-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7dc42-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7dc42-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dc42-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7dc42-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7dc42-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7dc42-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7dc42-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7dc42-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7dc42-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="7dc42-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7dc42-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7dc42-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7dc42-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7dc42-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7dc42-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7dc42-110">Elements and attributes</span></span>

<span data-ttu-id="7dc42-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="7dc42-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7dc42-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7dc42-112">Child elements</span></span>

|<span data-ttu-id="7dc42-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7dc42-113">**Element**</span></span>|<span data-ttu-id="7dc42-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7dc42-114">**Type**</span></span>|<span data-ttu-id="7dc42-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7dc42-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7dc42-116">Row</span><span class="sxs-lookup"><span data-stu-id="7dc42-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7dc42-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="7dc42-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7dc42-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7dc42-118">Attributes</span></span>

<span data-ttu-id="7dc42-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="7dc42-119">None.</span></span>
  

