---
title: Элемент weatherdata (схема расположения прогноза погоды в Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Определяет элемент прогноза погоды.
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540933"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="42633-103">Элемент weatherdata (схема расположения прогноза погоды в Outlook)</span><span class="sxs-lookup"><span data-stu-id="42633-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="42633-104">Определяет элемент прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="42633-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42633-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="42633-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42633-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="42633-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="42633-107">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="42633-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="42633-108">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="42633-108">**Schema file**</span></span> <br/> |<span data-ttu-id="42633-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="42633-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="42633-110">Определение</span><span class="sxs-lookup"><span data-stu-id="42633-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="42633-111">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="42633-111">Elements and attributes</span></span>

<span data-ttu-id="42633-112">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="42633-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="42633-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="42633-113">Parent elements</span></span>

<span data-ttu-id="42633-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="42633-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42633-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="42633-115">Child elements</span></span>

|<span data-ttu-id="42633-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="42633-116">**Element**</span></span>|<span data-ttu-id="42633-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="42633-117">**Type**</span></span>|<span data-ttu-id="42633-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="42633-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="42633-119">погода</span><span class="sxs-lookup"><span data-stu-id="42633-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="42633-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="42633-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="42633-121">Указывает расположение, в который будет сообщаться о погоде.</span><span class="sxs-lookup"><span data-stu-id="42633-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="42633-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="42633-122">Attributes</span></span>

<span data-ttu-id="42633-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="42633-123">None.</span></span>
  

