---
title: Masters_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: ee53a4c5ce07151b0ba58ebe08a4b69cca12d313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814204"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="ea8e7-102">Masters_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ea8e7-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ea8e7-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ea8e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea8e7-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ea8e7-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ea8e7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ea8e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ea8e7-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ea8e7-108">Нет</span><span class="sxs-lookup"><span data-stu-id="ea8e7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ea8e7-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ea8e7-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ea8e7-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ea8e7-110">Elements and attributes</span></span>

<span data-ttu-id="ea8e7-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ea8e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ea8e7-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ea8e7-112">Child elements</span></span>

|<span data-ttu-id="ea8e7-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-113">**Element**</span></span>|<span data-ttu-id="ea8e7-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-114">**Type**</span></span>|<span data-ttu-id="ea8e7-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea8e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea8e7-116">Образец</span><span class="sxs-lookup"><span data-stu-id="ea8e7-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ea8e7-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="ea8e7-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ea8e7-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="ea8e7-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ea8e7-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="ea8e7-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ea8e7-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ea8e7-120">Attributes</span></span>

<span data-ttu-id="ea8e7-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="ea8e7-121">None.</span></span>
  

