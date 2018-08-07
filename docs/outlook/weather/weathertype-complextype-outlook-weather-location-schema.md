---
title: weatherType complexType (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Определяет параметры о погоды расположения.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812935"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="5c70b-103">weatherType complexType (схема местоположения погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="5c70b-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="5c70b-104">Определяет параметры о погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="5c70b-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="5c70b-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5c70b-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c70b-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5c70b-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="5c70b-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5c70b-107">**Schema file**</span></span> <br/> |<span data-ttu-id="5c70b-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="5c70b-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="5c70b-109">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="5c70b-109">**Extension base**</span></span> <br/> |<span data-ttu-id="5c70b-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5c70b-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c70b-111">Определение</span><span class="sxs-lookup"><span data-stu-id="5c70b-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c70b-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5c70b-112">Elements and attributes</span></span>

<span data-ttu-id="5c70b-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="5c70b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5c70b-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5c70b-114">Child elements</span></span>

<span data-ttu-id="5c70b-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c70b-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c70b-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5c70b-116">Attributes</span></span>

|<span data-ttu-id="5c70b-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5c70b-117">**Attribute**</span></span>|<span data-ttu-id="5c70b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5c70b-118">**Type**</span></span>|<span data-ttu-id="5c70b-119">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="5c70b-119">**Required**</span></span>|<span data-ttu-id="5c70b-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c70b-120">**Description**</span></span>|<span data-ttu-id="5c70b-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5c70b-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c70b-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="5c70b-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="5c70b-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c70b-123">xs:string</span></span>  <br/> |<span data-ttu-id="5c70b-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c70b-124">required</span></span>  <br/> |<span data-ttu-id="5c70b-125">Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="5c70b-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="5c70b-126">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5c70b-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5c70b-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="5c70b-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="5c70b-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c70b-128">xs:string</span></span>  <br/> |<span data-ttu-id="5c70b-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c70b-129">required</span></span>  <br/> |<span data-ttu-id="5c70b-130">Указывает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="5c70b-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="5c70b-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5c70b-131">A value of the type xs:string</span></span>  <br/> |
   

