---
title: PageContents_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: ab74c646e72a7ebe5fbf5863c196d5b115be9b43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814333"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="bfa8f-102">PageContents_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bfa8f-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bfa8f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bfa8f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfa8f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bfa8f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bfa8f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bfa8f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bfa8f-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bfa8f-108">Нет</span><span class="sxs-lookup"><span data-stu-id="bfa8f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bfa8f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bfa8f-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bfa8f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bfa8f-110">Elements and attributes</span></span>

<span data-ttu-id="bfa8f-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bfa8f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bfa8f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bfa8f-112">Child elements</span></span>

|<span data-ttu-id="bfa8f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-113">**Element**</span></span>|<span data-ttu-id="bfa8f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-114">**Type**</span></span>|<span data-ttu-id="bfa8f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bfa8f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bfa8f-116">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="bfa8f-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bfa8f-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="bfa8f-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bfa8f-118">Фигур</span><span class="sxs-lookup"><span data-stu-id="bfa8f-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bfa8f-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="bfa8f-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bfa8f-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bfa8f-120">Attributes</span></span>

<span data-ttu-id="bfa8f-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="bfa8f-121">None.</span></span>
  

