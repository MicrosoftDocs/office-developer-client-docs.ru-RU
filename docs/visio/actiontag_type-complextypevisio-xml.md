---
title: ActionTag_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: a30290ee9dbb86c7af75820bd767bb95ce4add21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384775"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="54944-102">ActionTag_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="54944-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="54944-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="54944-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54944-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="54944-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="54944-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="54944-105">**Schema file**</span></span> <br/> |<span data-ttu-id="54944-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="54944-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="54944-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="54944-107">**Extension base**</span></span> <br/> |<span data-ttu-id="54944-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="54944-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54944-109">Определение</span><span class="sxs-lookup"><span data-stu-id="54944-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54944-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="54944-110">Elements and attributes</span></span>

<span data-ttu-id="54944-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="54944-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="54944-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="54944-112">Child elements</span></span>

|<span data-ttu-id="54944-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="54944-113">**Element**</span></span>|<span data-ttu-id="54944-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="54944-114">**Type**</span></span>|<span data-ttu-id="54944-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="54944-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54944-116">Строка</span><span class="sxs-lookup"><span data-stu-id="54944-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="54944-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="54944-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="54944-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="54944-118">Attributes</span></span>

<span data-ttu-id="54944-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="54944-119">None.</span></span>
  

