---
title: AuthorList_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 5df48bcc69f0bd4aa818f265d0c7db1986165b3e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537901"
---
# <a name="authorlist_type-complextype-visio-xml"></a><span data-ttu-id="77350-102">AuthorList_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="77350-102">AuthorList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="77350-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="77350-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77350-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="77350-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="77350-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="77350-105">**Schema file**</span></span> <br/> |<span data-ttu-id="77350-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="77350-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="77350-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="77350-107">**Extension base**</span></span> <br/> |<span data-ttu-id="77350-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="77350-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77350-109">Определение</span><span class="sxs-lookup"><span data-stu-id="77350-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="77350-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="77350-110">Elements and attributes</span></span>

<span data-ttu-id="77350-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="77350-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="77350-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="77350-112">Child elements</span></span>

|<span data-ttu-id="77350-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="77350-113">**Element**</span></span>|<span data-ttu-id="77350-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="77350-114">**Type**</span></span>|<span data-ttu-id="77350-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77350-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77350-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="77350-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="77350-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="77350-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="77350-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="77350-118">Attributes</span></span>

<span data-ttu-id="77350-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="77350-119">None.</span></span>
  

