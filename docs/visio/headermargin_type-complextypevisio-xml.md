---
title: Хеадермаргин_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330053"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="47a8b-102">Хеадермаргин_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="47a8b-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47a8b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="47a8b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47a8b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="47a8b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47a8b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="47a8b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47a8b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47a8b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47a8b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="47a8b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47a8b-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="47a8b-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47a8b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="47a8b-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47a8b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="47a8b-110">Elements and attributes</span></span>

<span data-ttu-id="47a8b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="47a8b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47a8b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="47a8b-112">Child elements</span></span>

<span data-ttu-id="47a8b-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="47a8b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47a8b-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="47a8b-114">Attributes</span></span>

|<span data-ttu-id="47a8b-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="47a8b-115">**Attribute**</span></span>|<span data-ttu-id="47a8b-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="47a8b-116">**Type**</span></span>|<span data-ttu-id="47a8b-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="47a8b-117">**Required**</span></span>|<span data-ttu-id="47a8b-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47a8b-118">**Description**</span></span>|<span data-ttu-id="47a8b-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="47a8b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47a8b-120">Устройств</span><span class="sxs-lookup"><span data-stu-id="47a8b-120">Unit</span></span>  <br/> |<span data-ttu-id="47a8b-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="47a8b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="47a8b-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="47a8b-122">optional</span></span>  <br/> ||<span data-ttu-id="47a8b-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="47a8b-123">Values of the xsd:string type.</span></span>  <br/> |
   

