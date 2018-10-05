---
title: Issues_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 42482db0c4542398381bc02ec5b21a8b80fac62f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397235"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="eac57-102">Issues_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="eac57-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="eac57-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="eac57-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eac57-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="eac57-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eac57-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="eac57-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eac57-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eac57-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eac57-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="eac57-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eac57-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="eac57-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eac57-109">Определение</span><span class="sxs-lookup"><span data-stu-id="eac57-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="eac57-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="eac57-110">Elements and attributes</span></span>

<span data-ttu-id="eac57-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="eac57-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eac57-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eac57-112">Child elements</span></span>

|<span data-ttu-id="eac57-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="eac57-113">**Element**</span></span>|<span data-ttu-id="eac57-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eac57-114">**Type**</span></span>|<span data-ttu-id="eac57-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eac57-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eac57-116">Проблема</span><span class="sxs-lookup"><span data-stu-id="eac57-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eac57-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="eac57-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="eac57-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eac57-118">Attributes</span></span>

<span data-ttu-id="eac57-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="eac57-119">None.</span></span>
  

