---
title: элемент веасердата (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Определяет элемент weather.
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355078"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="f0b99-103">элемент веасердата (схема сведений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="f0b99-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f0b99-104">Определяет элемент weather.</span><span class="sxs-lookup"><span data-stu-id="f0b99-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0b99-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f0b99-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0b99-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f0b99-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="f0b99-107">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f0b99-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f0b99-108">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f0b99-108">**Schema file**</span></span> <br/> |<span data-ttu-id="f0b99-109">жетвеасеринфо. xsd</span><span class="sxs-lookup"><span data-stu-id="f0b99-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0b99-110">Определение</span><span class="sxs-lookup"><span data-stu-id="f0b99-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0b99-111">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0b99-111">Elements and attributes</span></span>

<span data-ttu-id="f0b99-112">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f0b99-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f0b99-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f0b99-113">Parent elements</span></span>

<span data-ttu-id="f0b99-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="f0b99-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0b99-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f0b99-115">Child elements</span></span>

|<span data-ttu-id="f0b99-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f0b99-116">**Element**</span></span>|<span data-ttu-id="f0b99-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f0b99-117">**Type**</span></span>|<span data-ttu-id="f0b99-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0b99-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0b99-119">Погода</span><span class="sxs-lookup"><span data-stu-id="f0b99-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="f0b99-120">Веасертипе</span><span class="sxs-lookup"><span data-stu-id="f0b99-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="f0b99-121">Задает условия для расположения в прогнозе погоды.</span><span class="sxs-lookup"><span data-stu-id="f0b99-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f0b99-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0b99-122">Attributes</span></span>

<span data-ttu-id="f0b99-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="f0b99-123">None.</span></span>
  

