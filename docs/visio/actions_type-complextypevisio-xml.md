---
title: Актионс_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 384b948c61f3b618d108db090721ea6768d69372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538412"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="09e1e-102">Актионс_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="09e1e-102">Actions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="09e1e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="09e1e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09e1e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="09e1e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09e1e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="09e1e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09e1e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="09e1e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09e1e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="09e1e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09e1e-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="09e1e-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09e1e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="09e1e-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09e1e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="09e1e-110">Elements and attributes</span></span>

<span data-ttu-id="09e1e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="09e1e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09e1e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09e1e-112">Child elements</span></span>

|<span data-ttu-id="09e1e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="09e1e-113">**Element**</span></span>|<span data-ttu-id="09e1e-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="09e1e-114">**Type**</span></span>|<span data-ttu-id="09e1e-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09e1e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09e1e-116">Row</span><span class="sxs-lookup"><span data-stu-id="09e1e-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="09e1e-117">Актионсров_типе</span><span class="sxs-lookup"><span data-stu-id="09e1e-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="09e1e-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="09e1e-118">Attributes</span></span>

<span data-ttu-id="09e1e-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="09e1e-119">None.</span></span>
  

