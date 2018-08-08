---
title: элемент WeatherData (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Определяет элемент прогноза погоды.
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812952"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="ad8b5-103">элемент WeatherData (схема местоположения погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="ad8b5-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="ad8b5-104">Определяет элемент прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="ad8b5-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad8b5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ad8b5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad8b5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="ad8b5-107">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="ad8b5-108">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-108">**Schema file**</span></span> <br/> |<span data-ttu-id="ad8b5-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="ad8b5-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad8b5-110">Определение</span><span class="sxs-lookup"><span data-stu-id="ad8b5-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad8b5-111">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad8b5-111">Elements and attributes</span></span>

<span data-ttu-id="ad8b5-112">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ad8b5-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad8b5-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ad8b5-113">Parent elements</span></span>

<span data-ttu-id="ad8b5-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="ad8b5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad8b5-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ad8b5-115">Child elements</span></span>

|<span data-ttu-id="ad8b5-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-116">**Element**</span></span>|<span data-ttu-id="ad8b5-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-117">**Type**</span></span>|<span data-ttu-id="ad8b5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad8b5-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad8b5-119">прогноза погоды</span><span class="sxs-lookup"><span data-stu-id="ad8b5-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="ad8b5-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="ad8b5-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="ad8b5-121">Указывает местоположение для прогноза погоды отчет на.</span><span class="sxs-lookup"><span data-stu-id="ad8b5-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad8b5-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad8b5-122">Attributes</span></span>

<span data-ttu-id="ad8b5-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="ad8b5-123">None.</span></span>
  

