---
title: Формат TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Последнее изменение: 12 марта 2013 г.'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591935"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="62616-103">Формат TNEF</span><span class="sxs-lookup"><span data-stu-id="62616-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="62616-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62616-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62616-105">TNEF имеет формат для преобразования набор свойств MAPI — сообщение MAPI — в поток последовательных данных.</span><span class="sxs-lookup"><span data-stu-id="62616-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="62616-106">Функции TNEF в основном используются поставщиками транспорта, которые необходимы для кодирования свойства сообщений MAPI для передачи через системы обмена сообщениями, который не поддерживает эти свойства непосредственно.</span><span class="sxs-lookup"><span data-stu-id="62616-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="62616-107">Например транспорта на основе SMTP использует TNEF для кодирования свойства, такие как **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), не имеющими прямой представления в структуре SMTP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="62616-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="62616-108">Реализация TNEF определяет несколько TNEF особых атрибутов, каждый из которых соответствует конкретному свойству MAPI.</span><span class="sxs-lookup"><span data-stu-id="62616-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="62616-109">Эти атрибуты используются для кодирования их соответствующих свойств MAPI в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="62616-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="62616-110">Кроме того, определяется специальный атрибут, который можно использовать для инкапсуляции любого свойства MAPI, для которого не определенный атрибут, соответствующий его.</span><span class="sxs-lookup"><span data-stu-id="62616-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="62616-111">Эти атрибуты определены причину — вместо просто универсальный метод для всех свойств MAPI шифрования — — для обеспечения обратной совместимости с не MAPI-совместимое программное обеспечение, с помощью TNEF.</span><span class="sxs-lookup"><span data-stu-id="62616-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="62616-112">В оставшейся части этого раздела описываются структуры и синтаксис поток TNEF сопоставление свойств MAPI и атрибуты TNEF и рекомендации для определенных атрибутов TNEF.</span><span class="sxs-lookup"><span data-stu-id="62616-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

