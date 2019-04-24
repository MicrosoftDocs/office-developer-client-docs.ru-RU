---
title: Веасертипе complexType (схема расположения прогноза погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Определяет параметры для положения прогноза погоды.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355183"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="b124f-103">Веасертипе complexType (схема расположения прогноза погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="b124f-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="b124f-104">Определяет параметры для положения прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="b124f-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="b124f-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b124f-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b124f-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b124f-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="b124f-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b124f-107">**Schema file**</span></span> <br/> |<span data-ttu-id="b124f-108">жетвеасерлокатион. xsd</span><span class="sxs-lookup"><span data-stu-id="b124f-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="b124f-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b124f-109">**Extension base**</span></span> <br/> |<span data-ttu-id="b124f-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b124f-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b124f-111">Определение</span><span class="sxs-lookup"><span data-stu-id="b124f-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b124f-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b124f-112">Elements and attributes</span></span>

<span data-ttu-id="b124f-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b124f-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b124f-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b124f-114">Child elements</span></span>

<span data-ttu-id="b124f-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="b124f-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b124f-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b124f-116">Attributes</span></span>

|<span data-ttu-id="b124f-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b124f-117">**Attribute**</span></span>|<span data-ttu-id="b124f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b124f-118">**Type**</span></span>|<span data-ttu-id="b124f-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b124f-119">**Required**</span></span>|<span data-ttu-id="b124f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b124f-120">**Description**</span></span>|<span data-ttu-id="b124f-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b124f-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b124f-122">веасерлокатионкоде</span><span class="sxs-lookup"><span data-stu-id="b124f-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b124f-123">xs: String</span><span class="sxs-lookup"><span data-stu-id="b124f-123">xs:string</span></span>  <br/> |<span data-ttu-id="b124f-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b124f-124">required</span></span>  <br/> |<span data-ttu-id="b124f-125">Указывает код, связанный с расположением, для различения нескольких расположений с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="b124f-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="b124f-126">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="b124f-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b124f-127">веасерлокатионнаме</span><span class="sxs-lookup"><span data-stu-id="b124f-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b124f-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="b124f-128">xs:string</span></span>  <br/> |<span data-ttu-id="b124f-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b124f-129">required</span></span>  <br/> |<span data-ttu-id="b124f-130">Задает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="b124f-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="b124f-131">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="b124f-131">A value of the type xs:string</span></span>  <br/> |
   

