---
title: FaceNames_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 70ca3c5717ef6f85899a9be2ab4299dcefbd8fa0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542424"
---
# <a name="facenames_type-complextype-visio-xml"></a><span data-ttu-id="62164-102">FaceNames_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="62164-102">FaceNames_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="62164-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="62164-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62164-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="62164-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="62164-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="62164-105">**Schema file**</span></span> <br/> |<span data-ttu-id="62164-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="62164-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="62164-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="62164-107">**Extension base**</span></span> <br/> |<span data-ttu-id="62164-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="62164-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62164-109">Определение</span><span class="sxs-lookup"><span data-stu-id="62164-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62164-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="62164-110">Elements and attributes</span></span>

<span data-ttu-id="62164-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="62164-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62164-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62164-112">Child elements</span></span>

|<span data-ttu-id="62164-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="62164-113">**Element**</span></span>|<span data-ttu-id="62164-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62164-114">**Type**</span></span>|<span data-ttu-id="62164-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62164-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62164-116">FaceName</span><span class="sxs-lookup"><span data-stu-id="62164-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62164-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="62164-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="62164-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62164-118">Attributes</span></span>

<span data-ttu-id="62164-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="62164-119">None.</span></span>
  

