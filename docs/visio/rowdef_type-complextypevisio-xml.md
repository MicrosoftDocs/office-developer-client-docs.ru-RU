---
title: RowDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394589"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="573e5-102">RowDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="573e5-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="573e5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="573e5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="573e5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="573e5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="573e5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="573e5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="573e5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="573e5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="573e5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="573e5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="573e5-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="573e5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="573e5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="573e5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="573e5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="573e5-110">Elements and attributes</span></span>

<span data-ttu-id="573e5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="573e5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="573e5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="573e5-112">Child elements</span></span>

|<span data-ttu-id="573e5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="573e5-113">**Element**</span></span>|<span data-ttu-id="573e5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="573e5-114">**Type**</span></span>|<span data-ttu-id="573e5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="573e5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="573e5-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="573e5-116">CellDef</span></span> <br/> |[<span data-ttu-id="573e5-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="573e5-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="573e5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="573e5-118">Attributes</span></span>

<span data-ttu-id="573e5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="573e5-119">None.</span></span>
  

