---
title: Публишсеттингс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: eaa4bba1c5772b11fdbd2ec1c975f475e1c5d57a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360020"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="58d85-102">Публишсеттингс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="58d85-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="58d85-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="58d85-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58d85-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="58d85-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="58d85-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="58d85-105">**Schema file**</span></span> <br/> |<span data-ttu-id="58d85-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="58d85-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="58d85-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="58d85-107">**Extension base**</span></span> <br/> |<span data-ttu-id="58d85-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="58d85-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58d85-109">Определение</span><span class="sxs-lookup"><span data-stu-id="58d85-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="58d85-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="58d85-110">Elements and attributes</span></span>

<span data-ttu-id="58d85-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="58d85-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="58d85-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="58d85-112">Child elements</span></span>

|<span data-ttu-id="58d85-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="58d85-113">**Element**</span></span>|<span data-ttu-id="58d85-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58d85-114">**Type**</span></span>|<span data-ttu-id="58d85-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58d85-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58d85-116">Публишедпаже</span><span class="sxs-lookup"><span data-stu-id="58d85-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58d85-117">Публишедпаже_типе</span><span class="sxs-lookup"><span data-stu-id="58d85-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="58d85-118">Рефрешабледата</span><span class="sxs-lookup"><span data-stu-id="58d85-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58d85-119">Рефрешабледата_типе</span><span class="sxs-lookup"><span data-stu-id="58d85-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="58d85-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="58d85-120">Attributes</span></span>

<span data-ttu-id="58d85-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="58d85-121">None.</span></span>
  

