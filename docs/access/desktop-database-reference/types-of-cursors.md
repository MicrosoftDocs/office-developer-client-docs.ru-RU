---
title: Типы курсоров (Справочник по для настольных баз данных Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf41f9075e7716049a82818de930faa84cd0ae3e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945553"
---
# <a name="types-of-cursors"></a><span data-ttu-id="a9e98-102">Типы курсоров</span><span class="sxs-lookup"><span data-stu-id="a9e98-102">Types of cursors</span></span>


<span data-ttu-id="a9e98-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9e98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9e98-104">Как правило в приложении следует использовать простой курсор, который предоставляет доступ требуемых данных.</span><span class="sxs-lookup"><span data-stu-id="a9e98-104">As a general rule, your application should use the simplest cursor that provides the required data access.</span></span> <span data-ttu-id="a9e98-105">Каждой из которых дополнительные курсор от простого к сложному (только вперед, только для чтения, static, прокрутки, небуферизованные) имеет цену — в памяти клиента, сетевой нагрузки и производительности.</span><span class="sxs-lookup"><span data-stu-id="a9e98-105">Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance.</span></span> <span data-ttu-id="a9e98-106">Во многих случаях параметры курсора по умолчанию создать более сложных курсор не фактически приложению.</span><span class="sxs-lookup"><span data-stu-id="a9e98-106">In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="a9e98-107">Выбор типа курсора зависит от как приложение использует набор результатов и также некоторые рекомендации по проектированию, включая размера набора результатов, процент рекомендуется использовать данные, уровень конфиденциальности сообщения для изменения данных и производительности приложения требования к.</span><span class="sxs-lookup"><span data-stu-id="a9e98-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="a9e98-108">Самое простое Выбор курсора зависит от того, требуется ли изменение или просто Просмотр данных:</span><span class="sxs-lookup"><span data-stu-id="a9e98-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="a9e98-109">Если требуется прокручивать набор результатов, но не изменяют данные, используйте [только вперед](forward-only-cursors.md) или [статический](static-cursors.md) курсор.</span><span class="sxs-lookup"><span data-stu-id="a9e98-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="a9e98-110">Если у вас есть больших результатов задать и нужно выбрать только несколько строк, используйте курсор [набора ключей](keyset-cursors.md) .</span><span class="sxs-lookup"><span data-stu-id="a9e98-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="a9e98-111">Если вы хотите синхронизировать результирующий набор с последними добавляет, изменяет и удаляет всех параллельных пользователей, используйте [динамического](dynamic-cursors.md) курсора.</span><span class="sxs-lookup"><span data-stu-id="a9e98-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="a9e98-112">Несмотря на то, что каждый тип курсора кажется четкие, имейте в виду, что эти типы курсора не намного разных видов просто в результате перекрывающиеся характеристики и параметры.</span><span class="sxs-lookup"><span data-stu-id="a9e98-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

