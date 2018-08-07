---
title: Issues_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814009"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="8c296-102">Issues_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="8c296-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8c296-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8c296-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c296-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8c296-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8c296-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8c296-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8c296-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8c296-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8c296-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="8c296-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8c296-108">Нет</span><span class="sxs-lookup"><span data-stu-id="8c296-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c296-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8c296-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8c296-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c296-110">Elements and attributes</span></span>

<span data-ttu-id="8c296-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="8c296-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8c296-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8c296-112">Child elements</span></span>

|<span data-ttu-id="8c296-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8c296-113">**Element**</span></span>|<span data-ttu-id="8c296-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8c296-114">**Type**</span></span>|<span data-ttu-id="8c296-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c296-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c296-116">Проблема</span><span class="sxs-lookup"><span data-stu-id="8c296-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c296-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8c296-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8c296-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c296-118">Attributes</span></span>

<span data-ttu-id="8c296-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="8c296-119">None.</span></span>
  

