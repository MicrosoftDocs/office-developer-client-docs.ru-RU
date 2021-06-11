---
title: элемент weatherdata (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Определяет элемент погоды.
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538986"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="1f159-103">элемент weatherdata (Outlook схема сведений о погоде)</span><span class="sxs-lookup"><span data-stu-id="1f159-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="1f159-104">Определяет элемент погоды.</span><span class="sxs-lookup"><span data-stu-id="1f159-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f159-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1f159-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f159-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1f159-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="1f159-107">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1f159-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="1f159-108">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1f159-108">**Schema file**</span></span> <br/> |<span data-ttu-id="1f159-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="1f159-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f159-110">Определение</span><span class="sxs-lookup"><span data-stu-id="1f159-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1f159-111">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1f159-111">Elements and attributes</span></span>

<span data-ttu-id="1f159-112">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1f159-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1f159-113">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1f159-113">Parent elements</span></span>

<span data-ttu-id="1f159-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="1f159-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f159-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1f159-115">Child elements</span></span>

|<span data-ttu-id="1f159-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1f159-116">**Element**</span></span>|<span data-ttu-id="1f159-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1f159-117">**Type**</span></span>|<span data-ttu-id="1f159-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f159-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f159-119">погода</span><span class="sxs-lookup"><span data-stu-id="1f159-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="1f159-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="1f159-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="1f159-121">Указывает погодные условия расположения.</span><span class="sxs-lookup"><span data-stu-id="1f159-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1f159-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1f159-122">Attributes</span></span>

<span data-ttu-id="1f159-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="1f159-123">None.</span></span>
  

