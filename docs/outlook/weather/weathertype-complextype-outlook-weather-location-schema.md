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
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387715"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="9b492-103">weatherType complexType (схема местоположения погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="9b492-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="9b492-104">Определяет параметры о погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="9b492-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="9b492-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9b492-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b492-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9b492-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="9b492-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9b492-107">**Schema file**</span></span> <br/> |<span data-ttu-id="9b492-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="9b492-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="9b492-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9b492-109">**Extension base**</span></span> <br/> |<span data-ttu-id="9b492-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9b492-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b492-111">Определение</span><span class="sxs-lookup"><span data-stu-id="9b492-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="9b492-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9b492-112">Elements and attributes</span></span>

<span data-ttu-id="9b492-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9b492-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9b492-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9b492-114">Child elements</span></span>

<span data-ttu-id="9b492-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="9b492-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b492-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9b492-116">Attributes</span></span>

|<span data-ttu-id="9b492-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9b492-117">**Attribute**</span></span>|<span data-ttu-id="9b492-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9b492-118">**Type**</span></span>|<span data-ttu-id="9b492-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9b492-119">**Required**</span></span>|<span data-ttu-id="9b492-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b492-120">**Description**</span></span>|<span data-ttu-id="9b492-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9b492-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9b492-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="9b492-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="9b492-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="9b492-123">xs:string</span></span>  <br/> |<span data-ttu-id="9b492-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9b492-124">required</span></span>  <br/> |<span data-ttu-id="9b492-125">Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="9b492-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="9b492-126">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="9b492-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9b492-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="9b492-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="9b492-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="9b492-128">xs:string</span></span>  <br/> |<span data-ttu-id="9b492-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9b492-129">required</span></span>  <br/> |<span data-ttu-id="9b492-130">Указывает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="9b492-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="9b492-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="9b492-131">A value of the type xs:string</span></span>  <br/> |
   

