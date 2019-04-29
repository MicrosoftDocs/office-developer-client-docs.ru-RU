---
title: Формат TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Дата последнего изменения: 12 марта 2013 г.'
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428692"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="8bb26-103">Формат TNEF</span><span class="sxs-lookup"><span data-stu-id="8bb26-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="8bb26-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bb26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bb26-105">Формат TNEF — это формат, служащий для преобразования набора параметров MAPI — сообщения MAPI — в поток последовательных данных.</span><span class="sxs-lookup"><span data-stu-id="8bb26-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="8bb26-106">Функции TNEF в основном используются поставщиками транспорта, которые нуждаются в кодировании свойств сообщений MAPI для передачи через систему обмена сообщениями, которая не поддерживает эти свойства напрямую.</span><span class="sxs-lookup"><span data-stu-id="8bb26-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="8bb26-107">Например, транспорт на основе SMTP использует TNEF для кодирования свойств, таких как **пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), которые не имеют прямого представления в структуре SMTP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="8bb26-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="8bb26-108">Реализация TNEF определяет несколько атрибутов TNEF, каждый из которых соответствует определенному свойству MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bb26-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="8bb26-109">Эти атрибуты используются для кодирования соответствующих свойств MAPI в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="8bb26-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="8bb26-110">Кроме того, определен специальный атрибут, который можно использовать для инкапсуляции любого свойства MAPI, для которого не определен соответствующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="8bb26-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="8bb26-111">Причина, по которой эти атрибуты определены, вместо простого использования единообразного метода кодирования для всех свойств MAPI — это обеспечение обратной совместимости с программным обеспечением, не совместимым с MAPI, которое использует формат TNEF.</span><span class="sxs-lookup"><span data-stu-id="8bb26-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="8bb26-112">В оставшейся части этого раздела описывается структура и синтаксис потока TNEF, сопоставление между свойствами MAPI и атрибутами TNEF, а также важные рекомендации по некоторым атрибутам TNEF.</span><span class="sxs-lookup"><span data-stu-id="8bb26-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

