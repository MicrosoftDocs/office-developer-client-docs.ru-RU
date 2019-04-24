---
title: Стилешитс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346783"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="cfbc8-102">Стилешитс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cfbc8-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cfbc8-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="cfbc8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfbc8-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cfbc8-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cfbc8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cfbc8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cfbc8-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cfbc8-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="cfbc8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cfbc8-109">Определение</span><span class="sxs-lookup"><span data-stu-id="cfbc8-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cfbc8-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cfbc8-110">Elements and attributes</span></span>

<span data-ttu-id="cfbc8-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="cfbc8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cfbc8-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cfbc8-112">Child elements</span></span>

|<span data-ttu-id="cfbc8-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-113">**Element**</span></span>|<span data-ttu-id="cfbc8-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-114">**Type**</span></span>|<span data-ttu-id="cfbc8-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cfbc8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cfbc8-116">Применение</span><span class="sxs-lookup"><span data-stu-id="cfbc8-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cfbc8-117">Стилешит_типе</span><span class="sxs-lookup"><span data-stu-id="cfbc8-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cfbc8-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cfbc8-118">Attributes</span></span>

<span data-ttu-id="cfbc8-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="cfbc8-119">None.</span></span>
  

