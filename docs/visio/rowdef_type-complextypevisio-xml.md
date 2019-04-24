---
title: Ровдеф_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355771"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="76d41-102">Ровдеф_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="76d41-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="76d41-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="76d41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76d41-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="76d41-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="76d41-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="76d41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="76d41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="76d41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="76d41-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="76d41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="76d41-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="76d41-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76d41-109">Определение</span><span class="sxs-lookup"><span data-stu-id="76d41-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="76d41-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="76d41-110">Elements and attributes</span></span>

<span data-ttu-id="76d41-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="76d41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="76d41-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76d41-112">Child elements</span></span>

|<span data-ttu-id="76d41-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="76d41-113">**Element**</span></span>|<span data-ttu-id="76d41-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76d41-114">**Type**</span></span>|<span data-ttu-id="76d41-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76d41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76d41-116">Целлдеф</span><span class="sxs-lookup"><span data-stu-id="76d41-116">CellDef</span></span> <br/> |[<span data-ttu-id="76d41-117">Целлдеф_типе</span><span class="sxs-lookup"><span data-stu-id="76d41-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="76d41-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76d41-118">Attributes</span></span>

<span data-ttu-id="76d41-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="76d41-119">None.</span></span>
  

