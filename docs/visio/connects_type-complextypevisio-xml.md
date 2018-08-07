---
title: Connects_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: 4d2740bc0ee0934b28bbebbc10ca9c861c563be0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813477"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="11f26-102">Connects_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="11f26-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="11f26-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="11f26-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11f26-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="11f26-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11f26-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="11f26-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11f26-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11f26-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11f26-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="11f26-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11f26-108">Нет</span><span class="sxs-lookup"><span data-stu-id="11f26-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11f26-109">Определение</span><span class="sxs-lookup"><span data-stu-id="11f26-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11f26-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="11f26-110">Elements and attributes</span></span>

<span data-ttu-id="11f26-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="11f26-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11f26-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="11f26-112">Child elements</span></span>

|<span data-ttu-id="11f26-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="11f26-113">**Element**</span></span>|<span data-ttu-id="11f26-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="11f26-114">**Type**</span></span>|<span data-ttu-id="11f26-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="11f26-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11f26-116">Подключение</span><span class="sxs-lookup"><span data-stu-id="11f26-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11f26-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="11f26-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="11f26-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="11f26-118">Attributes</span></span>

<span data-ttu-id="11f26-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="11f26-119">None.</span></span>
  

