---
title: Scratch_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 973a0db86eec553c7a728095e28735d4cdb91041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814723"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="00c66-102">Scratch_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="00c66-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="00c66-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="00c66-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00c66-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="00c66-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="00c66-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="00c66-105">**Schema file**</span></span> <br/> |<span data-ttu-id="00c66-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="00c66-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="00c66-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="00c66-107">**Extension base**</span></span> <br/> |<span data-ttu-id="00c66-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="00c66-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00c66-109">Определение</span><span class="sxs-lookup"><span data-stu-id="00c66-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="00c66-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="00c66-110">Elements and attributes</span></span>

<span data-ttu-id="00c66-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="00c66-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="00c66-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="00c66-112">Child elements</span></span>

|<span data-ttu-id="00c66-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="00c66-113">**Element**</span></span>|<span data-ttu-id="00c66-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="00c66-114">**Type**</span></span>|<span data-ttu-id="00c66-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00c66-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="00c66-116">Row</span><span class="sxs-lookup"><span data-stu-id="00c66-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="00c66-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="00c66-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="00c66-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="00c66-118">Attributes</span></span>

<span data-ttu-id="00c66-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="00c66-119">None.</span></span>
  

