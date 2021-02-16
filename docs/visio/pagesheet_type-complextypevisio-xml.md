---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540590"
---
# <a name="pagesheet_type-complextype-visio-xml"></a><span data-ttu-id="fef36-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fef36-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fef36-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="fef36-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fef36-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fef36-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fef36-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fef36-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fef36-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fef36-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fef36-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="fef36-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fef36-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="fef36-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fef36-109">Определение</span><span class="sxs-lookup"><span data-stu-id="fef36-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fef36-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fef36-110">Elements and attributes</span></span>

<span data-ttu-id="fef36-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fef36-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fef36-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fef36-112">Child elements</span></span>

<span data-ttu-id="fef36-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="fef36-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fef36-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fef36-114">Attributes</span></span>

|<span data-ttu-id="fef36-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fef36-115">**Attribute**</span></span>|<span data-ttu-id="fef36-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fef36-116">**Type**</span></span>|<span data-ttu-id="fef36-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fef36-117">**Required**</span></span>|<span data-ttu-id="fef36-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fef36-118">**Description**</span></span>|<span data-ttu-id="fef36-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fef36-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fef36-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="fef36-120">UniqueID</span></span>  <br/> |<span data-ttu-id="fef36-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fef36-121">xsd:string</span></span>  <br/> |<span data-ttu-id="fef36-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="fef36-122">optional</span></span>  <br/> ||<span data-ttu-id="fef36-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fef36-123">Values of the xsd:string type.</span></span>  <br/> |
   

