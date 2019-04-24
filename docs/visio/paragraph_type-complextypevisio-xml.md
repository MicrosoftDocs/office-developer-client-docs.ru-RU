---
title: Параграф_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 8a57a0df516f998e4e815240f1405962e11f848d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338810"
---
# <a name="paragraphtype-complextype-visio-xml"></a><span data-ttu-id="ce5a5-102">Параграф_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ce5a5-102">Paragraph_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ce5a5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ce5a5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce5a5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ce5a5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ce5a5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ce5a5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ce5a5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ce5a5-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="ce5a5-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce5a5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ce5a5-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ce5a5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ce5a5-110">Elements and attributes</span></span>

<span data-ttu-id="ce5a5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ce5a5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ce5a5-112">Child elements</span></span>

|<span data-ttu-id="ce5a5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-113">**Element**</span></span>|<span data-ttu-id="ce5a5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-114">**Type**</span></span>|<span data-ttu-id="ce5a5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce5a5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce5a5-116">Row</span><span class="sxs-lookup"><span data-stu-id="ce5a5-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ce5a5-117">Параграфров_типе</span><span class="sxs-lookup"><span data-stu-id="ce5a5-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ce5a5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ce5a5-118">Attributes</span></span>

<span data-ttu-id="ce5a5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-119">None.</span></span>
  

