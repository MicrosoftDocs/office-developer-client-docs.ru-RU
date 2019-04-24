---
title: Иссуес_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 42482db0c4542398381bc02ec5b21a8b80fac62f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339475"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="27341-102">Иссуес_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="27341-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="27341-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="27341-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27341-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="27341-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="27341-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="27341-105">**Schema file**</span></span> <br/> |<span data-ttu-id="27341-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="27341-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="27341-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="27341-107">**Extension base**</span></span> <br/> |<span data-ttu-id="27341-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="27341-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27341-109">Определение</span><span class="sxs-lookup"><span data-stu-id="27341-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27341-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="27341-110">Elements and attributes</span></span>

<span data-ttu-id="27341-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="27341-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="27341-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="27341-112">Child elements</span></span>

|<span data-ttu-id="27341-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="27341-113">**Element**</span></span>|<span data-ttu-id="27341-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="27341-114">**Type**</span></span>|<span data-ttu-id="27341-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="27341-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27341-116">Проблема</span><span class="sxs-lookup"><span data-stu-id="27341-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27341-117">Иссуе_типе</span><span class="sxs-lookup"><span data-stu-id="27341-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="27341-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="27341-118">Attributes</span></span>

<span data-ttu-id="27341-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="27341-119">None.</span></span>
  

