---
title: Идентификаторы и типы свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437219"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="bd1ea-103">Идентификаторы и типы свойств</span><span class="sxs-lookup"><span data-stu-id="bd1ea-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="bd1ea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd1ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd1ea-105">Все свойства MAPI представлены тегами свойств.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="bd1ea-106">Тег свойства — это 32-битное неподписаное значение, которое содержит идентификатор свойства в 16 битах высокого порядка, а тип свойства в низком порядке — в 16 битах.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="bd1ea-107">Теги свойств для всех свойств, определенных MAPI, включаются в файл загона mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="bd1ea-108">Идентификаторы свойств используются для того, чтобы указать, для чего используется свойство и кто несет за него ответственность.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="bd1ea-109">Идентификаторы свойств разделены по MAPI на диапазоны; где идентификатор попадает в диапазон, указывает на его использование и право собственности.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="bd1ea-110">Типы свойств используются для указать формат данных свойства.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="bd1ea-111">MAPI определяет все допустимые типы.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="bd1ea-112">Клиенты и поставщики услуг, создав новые свойства, должны использовать один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="bd1ea-113">Все типы свойств включены в файл загона mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="bd1ea-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

