---
title: PageSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814348"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="2978b-102">PageSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2978b-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2978b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2978b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2978b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2978b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2978b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2978b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2978b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2978b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2978b-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="2978b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2978b-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="2978b-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2978b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2978b-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2978b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2978b-110">Elements and attributes</span></span>

<span data-ttu-id="2978b-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="2978b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2978b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2978b-112">Child elements</span></span>

<span data-ttu-id="2978b-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="2978b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2978b-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2978b-114">Attributes</span></span>

|<span data-ttu-id="2978b-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="2978b-115">**Attribute**</span></span>|<span data-ttu-id="2978b-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2978b-116">**Type**</span></span>|<span data-ttu-id="2978b-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="2978b-117">**Required**</span></span>|<span data-ttu-id="2978b-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2978b-118">**Description**</span></span>|<span data-ttu-id="2978b-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="2978b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2978b-120">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="2978b-120">UniqueID</span></span>  <br/> |<span data-ttu-id="2978b-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2978b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="2978b-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="2978b-122">optional</span></span>  <br/> ||<span data-ttu-id="2978b-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2978b-123">Values of the xsd:string type.</span></span>  <br/> |
   

