---
title: Типы и идентификаторы свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 423992e0485e8e3092cfc4126164576906d51149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567065"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="2a22b-103">Типы и идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="2a22b-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="2a22b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a22b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a22b-105">Все свойства MAPI, представлены тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="2a22b-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="2a22b-106">Свойство tag — это значение 32-разрядное целое число, содержащее идентификатор свойства в высоким заказ 16-разрядный и тип свойства в небольшой упорядочивания 16 бит.</span><span class="sxs-lookup"><span data-stu-id="2a22b-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="2a22b-107">Теги свойства для всех свойств, определенных в MAPI включены в файл заголовка mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="2a22b-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="2a22b-108">Идентификаторы свойств используются для указания, для чего используется свойство и кто несет ответственность за его.</span><span class="sxs-lookup"><span data-stu-id="2a22b-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="2a22b-109">Идентификаторы свойств, разделены на с MAPI диапазонов; где идентификатор попадают в диапазон указывает его использованием и владельца.</span><span class="sxs-lookup"><span data-stu-id="2a22b-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="2a22b-110">Типы свойств используются для указания формата данных свойства.</span><span class="sxs-lookup"><span data-stu-id="2a22b-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="2a22b-111">MAPI определяет все из допустимых типов.</span><span class="sxs-lookup"><span data-stu-id="2a22b-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="2a22b-112">Клиенты и поставщиков услуг, создание новых свойств необходимо использовать один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="2a22b-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="2a22b-113">Включаются все типы свойств в файле заголовка mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="2a22b-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

