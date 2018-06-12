---
title: Идентификаторы свойств и типов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812068"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="dadf7-103">Идентификаторы свойств и типов</span><span class="sxs-lookup"><span data-stu-id="dadf7-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="dadf7-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dadf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dadf7-105">Все свойства MAPI, представлены тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="dadf7-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="dadf7-106">Свойство tag — это значение 32-разрядное целое число, содержащее идентификатор свойства в высоким заказ 16-разрядный и тип свойства в небольшой упорядочивания 16 бит.</span><span class="sxs-lookup"><span data-stu-id="dadf7-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="dadf7-107">Теги свойства для всех свойств, определенных в MAPI включены в файл заголовка mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="dadf7-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="dadf7-108">Идентификаторы свойств используются для указания, для чего используется свойство и кто несет ответственность за его.</span><span class="sxs-lookup"><span data-stu-id="dadf7-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="dadf7-109">Идентификаторы свойств, разделены на с MAPI диапазонов; где идентификатор попадают в диапазон указывает его использованием и владельца.</span><span class="sxs-lookup"><span data-stu-id="dadf7-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="dadf7-110">Типы свойств используются для указания формата данных свойства.</span><span class="sxs-lookup"><span data-stu-id="dadf7-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="dadf7-111">MAPI определяет все из допустимых типов.</span><span class="sxs-lookup"><span data-stu-id="dadf7-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="dadf7-112">Клиенты и поставщиков услуг, создание новых свойств необходимо использовать один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="dadf7-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="dadf7-113">Включаются все типы свойств в файле заголовка mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="dadf7-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

