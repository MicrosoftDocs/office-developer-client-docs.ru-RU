---
title: Типы курсоров (Справочник по для настольных баз данных Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717575"
---
# <a name="types-of-cursors"></a><span data-ttu-id="03648-102">Типы курсоров</span><span class="sxs-lookup"><span data-stu-id="03648-102">Types of cursors</span></span>


<span data-ttu-id="03648-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03648-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03648-104">Как правило в приложении следует использовать простой курсор, который предоставляет доступ требуемых данных.</span><span class="sxs-lookup"><span data-stu-id="03648-104">As a general rule, your application should use the simplest cursor that provides the required data access.</span></span> <span data-ttu-id="03648-105">Каждой из которых дополнительные курсор от простого к сложному (только вперед, только для чтения, static, прокрутки, небуферизованные) имеет цену — в памяти клиента, сетевой нагрузки и производительности.</span><span class="sxs-lookup"><span data-stu-id="03648-105">Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance.</span></span> <span data-ttu-id="03648-106">Во многих случаях параметры курсора по умолчанию создать более сложных курсор не фактически приложению.</span><span class="sxs-lookup"><span data-stu-id="03648-106">In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="03648-107">Выбор типа курсора зависит от как приложение использует набор результатов и также некоторые рекомендации по проектированию, включая размера набора результатов, процент рекомендуется использовать данные, уровень конфиденциальности сообщения для изменения данных и производительности приложения требования к.</span><span class="sxs-lookup"><span data-stu-id="03648-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="03648-108">Самое простое Выбор курсора зависит от того, требуется ли изменение или просто Просмотр данных:</span><span class="sxs-lookup"><span data-stu-id="03648-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="03648-109">Если требуется прокручивать набор результатов, но не изменяют данные, используйте [только вперед](forward-only-cursors.md) или [статический](static-cursors.md) курсор.</span><span class="sxs-lookup"><span data-stu-id="03648-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="03648-110">Если у вас есть больших результатов задать и нужно выбрать только несколько строк, используйте курсор [набора ключей](keyset-cursors.md) .</span><span class="sxs-lookup"><span data-stu-id="03648-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="03648-111">Если вы хотите синхронизировать результирующий набор с последними добавляет, изменяет и удаляет всех параллельных пользователей, используйте [динамического](dynamic-cursors.md) курсора.</span><span class="sxs-lookup"><span data-stu-id="03648-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="03648-112">Несмотря на то, что каждый тип курсора кажется четкие, имейте в виду, что эти типы курсора не намного разных видов просто в результате перекрывающиеся характеристики и параметры.</span><span class="sxs-lookup"><span data-stu-id="03648-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

