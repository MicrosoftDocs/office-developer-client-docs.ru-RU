---
title: Character_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: 0605298eadf57492b4af4ce1c987f01a9130281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813377"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="08614-102">Character_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="08614-102">Character_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="08614-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="08614-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08614-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="08614-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08614-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="08614-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08614-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="08614-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08614-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="08614-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08614-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="08614-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08614-109">Определение</span><span class="sxs-lookup"><span data-stu-id="08614-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08614-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="08614-110">Elements and attributes</span></span>

<span data-ttu-id="08614-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="08614-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08614-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="08614-112">Child elements</span></span>

|<span data-ttu-id="08614-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="08614-113">**Element**</span></span>|<span data-ttu-id="08614-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="08614-114">**Type**</span></span>|<span data-ttu-id="08614-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="08614-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08614-116">Row</span><span class="sxs-lookup"><span data-stu-id="08614-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="08614-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="08614-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="08614-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="08614-118">Attributes</span></span>

<span data-ttu-id="08614-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="08614-119">None.</span></span>
  

