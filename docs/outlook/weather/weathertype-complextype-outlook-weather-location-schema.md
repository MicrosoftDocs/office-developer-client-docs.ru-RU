---
title: weatherType complexType (Outlook схема расположения погоды)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Определяет параметры погодных условий расположения.
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542921"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="93639-103">weatherType complexType (Outlook схема расположения погоды)</span><span class="sxs-lookup"><span data-stu-id="93639-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="93639-104">Определяет параметры погодных условий расположения.</span><span class="sxs-lookup"><span data-stu-id="93639-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="93639-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="93639-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93639-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="93639-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="93639-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="93639-107">**Schema file**</span></span> <br/> |<span data-ttu-id="93639-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="93639-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="93639-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="93639-109">**Extension base**</span></span> <br/> |<span data-ttu-id="93639-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="93639-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93639-111">Определение</span><span class="sxs-lookup"><span data-stu-id="93639-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="93639-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="93639-112">Elements and attributes</span></span>

<span data-ttu-id="93639-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="93639-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="93639-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="93639-114">Child elements</span></span>

<span data-ttu-id="93639-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="93639-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93639-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="93639-116">Attributes</span></span>

|<span data-ttu-id="93639-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="93639-117">**Attribute**</span></span>|<span data-ttu-id="93639-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93639-118">**Type**</span></span>|<span data-ttu-id="93639-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="93639-119">**Required**</span></span>|<span data-ttu-id="93639-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93639-120">**Description**</span></span>|<span data-ttu-id="93639-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="93639-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="93639-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="93639-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="93639-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="93639-123">xs:string</span></span>  <br/> |<span data-ttu-id="93639-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="93639-124">required</span></span>  <br/> |<span data-ttu-id="93639-125">Указывает код, связанный с расположением, чтобы различать несколько расположений с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="93639-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="93639-126">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="93639-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="93639-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="93639-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="93639-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="93639-128">xs:string</span></span>  <br/> |<span data-ttu-id="93639-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="93639-129">required</span></span>  <br/> |<span data-ttu-id="93639-130">Указывает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="93639-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="93639-131">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="93639-131">A value of the type xs:string</span></span>  <br/> |
   

