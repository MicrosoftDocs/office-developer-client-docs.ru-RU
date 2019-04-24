---
title: элемент веасердата (схема расположений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Определяет элемент weather.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355036"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="6759c-103">элемент веасердата (схема расположений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="6759c-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="6759c-104">Определяет элемент weather.</span><span class="sxs-lookup"><span data-stu-id="6759c-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6759c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6759c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6759c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6759c-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="6759c-107">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6759c-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="6759c-108">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6759c-108">**Schema file**</span></span> <br/> |<span data-ttu-id="6759c-109">жетвеасерлокатион. xsd</span><span class="sxs-lookup"><span data-stu-id="6759c-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6759c-110">Определение</span><span class="sxs-lookup"><span data-stu-id="6759c-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6759c-111">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6759c-111">Elements and attributes</span></span>

<span data-ttu-id="6759c-112">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6759c-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6759c-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6759c-113">Parent elements</span></span>

<span data-ttu-id="6759c-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="6759c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6759c-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6759c-115">Child elements</span></span>

|<span data-ttu-id="6759c-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6759c-116">**Element**</span></span>|<span data-ttu-id="6759c-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6759c-117">**Type**</span></span>|<span data-ttu-id="6759c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6759c-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6759c-119">Погода</span><span class="sxs-lookup"><span data-stu-id="6759c-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="6759c-120">Веасертипе</span><span class="sxs-lookup"><span data-stu-id="6759c-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="6759c-121">Указывает расположение для отчета о погоде.</span><span class="sxs-lookup"><span data-stu-id="6759c-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6759c-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6759c-122">Attributes</span></span>

<span data-ttu-id="6759c-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="6759c-123">None.</span></span>
  

