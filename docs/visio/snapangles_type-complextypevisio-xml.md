---
title: SnapAngles_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1110a656-d8cd-19d0-1af0-31a6675bf89b
ms.openlocfilehash: 1ea5c6d907bf3b3af5664ce3c6f97dfbaa3fd442
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540359"
---
# <a name="snapangles_type-complextype-visio-xml"></a><span data-ttu-id="6ea9a-102">SnapAngles_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6ea9a-102">SnapAngles_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6ea9a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6ea9a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ea9a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6ea9a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6ea9a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6ea9a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6ea9a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6ea9a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="6ea9a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ea9a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6ea9a-109">Definition</span></span>

```XML
          <xs:complexType name="SnapAngles_Type">
          
          <xs:sequence>
    <xs:element name="SnapAngle"  type="SnapAngle_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ea9a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ea9a-110">Elements and attributes</span></span>

<span data-ttu-id="6ea9a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6ea9a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6ea9a-112">Child elements</span></span>

|<span data-ttu-id="6ea9a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-113">**Element**</span></span>|<span data-ttu-id="6ea9a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-114">**Type**</span></span>|<span data-ttu-id="6ea9a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ea9a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ea9a-116">снапангле</span><span class="sxs-lookup"><span data-stu-id="6ea9a-116">SnapAngle</span></span>](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ea9a-117">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="6ea9a-117">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6ea9a-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ea9a-118">Attributes</span></span>

<span data-ttu-id="6ea9a-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-119">None.</span></span>
  

