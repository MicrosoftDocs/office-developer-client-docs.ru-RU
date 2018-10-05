---
title: PageContents_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: 70f28182d8c82b9283e793856f7944c9a4823bc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383431"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="30d6a-102">PageContents_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="30d6a-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="30d6a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="30d6a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30d6a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="30d6a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="30d6a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="30d6a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="30d6a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="30d6a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="30d6a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="30d6a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="30d6a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="30d6a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30d6a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="30d6a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="30d6a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="30d6a-110">Elements and attributes</span></span>

<span data-ttu-id="30d6a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="30d6a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="30d6a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="30d6a-112">Child elements</span></span>

|<span data-ttu-id="30d6a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="30d6a-113">**Element**</span></span>|<span data-ttu-id="30d6a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="30d6a-114">**Type**</span></span>|<span data-ttu-id="30d6a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="30d6a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30d6a-116">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="30d6a-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30d6a-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="30d6a-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30d6a-118">Фигур</span><span class="sxs-lookup"><span data-stu-id="30d6a-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30d6a-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="30d6a-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="30d6a-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="30d6a-120">Attributes</span></span>

<span data-ttu-id="30d6a-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="30d6a-121">None.</span></span>
  

