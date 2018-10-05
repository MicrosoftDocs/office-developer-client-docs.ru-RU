---
title: FaceNames_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 6f9cd84dffc22f4211a8445a2d493ef7d4f4a4f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387148"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="c7cb6-102">FaceNames_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c7cb6-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c7cb6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c7cb6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7cb6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c7cb6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c7cb6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c7cb6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c7cb6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c7cb6-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="c7cb6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c7cb6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c7cb6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c7cb6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c7cb6-110">Elements and attributes</span></span>

<span data-ttu-id="c7cb6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c7cb6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c7cb6-112">Child elements</span></span>

|<span data-ttu-id="c7cb6-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-113">**Element**</span></span>|<span data-ttu-id="c7cb6-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-114">**Type**</span></span>|<span data-ttu-id="c7cb6-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c7cb6-116">Название значка</span><span class="sxs-lookup"><span data-stu-id="c7cb6-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c7cb6-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="c7cb6-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c7cb6-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c7cb6-118">Attributes</span></span>

<span data-ttu-id="c7cb6-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-119">None.</span></span>
  

