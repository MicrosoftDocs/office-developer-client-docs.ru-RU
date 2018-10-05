---
title: TabsRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: fed6c70119007164113ba76296bed5662e331c17
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395324"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="ec9a1-102">TabsRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ec9a1-102">TabsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec9a1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ec9a1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec9a1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec9a1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec9a1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec9a1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec9a1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec9a1-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="ec9a1-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec9a1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ec9a1-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec9a1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec9a1-110">Elements and attributes</span></span>

<span data-ttu-id="ec9a1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ec9a1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec9a1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec9a1-112">Child elements</span></span>

|<span data-ttu-id="ec9a1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-113">**Element**</span></span>|<span data-ttu-id="ec9a1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-114">**Type**</span></span>|<span data-ttu-id="ec9a1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec9a1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec9a1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ec9a1-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ec9a1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ec9a1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec9a1-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec9a1-118">Attributes</span></span>

<span data-ttu-id="ec9a1-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="ec9a1-119">None.</span></span>
  

