---
title: RowDef_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 79a01d9fe5edf1de933f05683eca3bfd6e95e4b3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538139"
---
# <a name="rowdef_type-complextype-visio-xml"></a><span data-ttu-id="9da5c-102">RowDef_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="9da5c-102">RowDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9da5c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9da5c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9da5c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9da5c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9da5c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9da5c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9da5c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9da5c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9da5c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9da5c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9da5c-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9da5c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9da5c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9da5c-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9da5c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9da5c-110">Elements and attributes</span></span>

<span data-ttu-id="9da5c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9da5c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9da5c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9da5c-112">Child elements</span></span>

|<span data-ttu-id="9da5c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9da5c-113">**Element**</span></span>|<span data-ttu-id="9da5c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9da5c-114">**Type**</span></span>|<span data-ttu-id="9da5c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9da5c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9da5c-116">целлдеф</span><span class="sxs-lookup"><span data-stu-id="9da5c-116">CellDef</span></span> <br/> |[<span data-ttu-id="9da5c-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="9da5c-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9da5c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9da5c-118">Attributes</span></span>

<span data-ttu-id="9da5c-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="9da5c-119">None.</span></span>
  

