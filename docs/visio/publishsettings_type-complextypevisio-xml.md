---
title: PublishSettings_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 6e9974d35b904581d43f481a02b8a3adee811730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814507"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="c9cc5-102">PublishSettings_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c9cc5-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c9cc5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c9cc5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9cc5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9cc5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9cc5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9cc5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9cc5-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9cc5-108">Нет</span><span class="sxs-lookup"><span data-stu-id="c9cc5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9cc5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c9cc5-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c9cc5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c9cc5-110">Elements and attributes</span></span>

<span data-ttu-id="c9cc5-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="c9cc5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9cc5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c9cc5-112">Child elements</span></span>

|<span data-ttu-id="c9cc5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-113">**Element**</span></span>|<span data-ttu-id="c9cc5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-114">**Type**</span></span>|<span data-ttu-id="c9cc5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c9cc5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c9cc5-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="c9cc5-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9cc5-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="c9cc5-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9cc5-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="c9cc5-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9cc5-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="c9cc5-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9cc5-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c9cc5-120">Attributes</span></span>

<span data-ttu-id="c9cc5-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9cc5-121">None.</span></span>
  

