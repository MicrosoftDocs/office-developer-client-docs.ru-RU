---
title: Типы курсоров (справочник по базам данных Access для настольных ПК)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314030"
---
# <a name="types-of-cursors"></a><span data-ttu-id="0e68f-102">Типы курсоров</span><span class="sxs-lookup"><span data-stu-id="0e68f-102">Types of cursors</span></span>


<span data-ttu-id="0e68f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e68f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e68f-104">Как правило, приложение должно использовать самый простой курсор, который обеспечивает необходимый доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="0e68f-104">As a general rule, your application should use the simplest cursor that provides the required data access.</span></span> <span data-ttu-id="0e68f-105">Каждая дополнительная характеристика курсора помимо базовых (только для чтения, только для чтения, статическая, прокрутка, отладка) имеет цену — в памяти клиента, сетевой нагрузке или производительности.</span><span class="sxs-lookup"><span data-stu-id="0e68f-105">Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance.</span></span> <span data-ttu-id="0e68f-106">Во многих случаях параметры курсора по умолчанию создают более сложный курсор, чем требуется приложению.</span><span class="sxs-lookup"><span data-stu-id="0e68f-106">In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="0e68f-107">Выбор типа курсора зависит от того, как приложение использует набор результатов, а также от нескольких аспектов проектирования, включая размер набора результатов, процент используемых данных, чувствительность к изменениям данных и требования к производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="0e68f-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="0e68f-108">По большей части выбор курсора зависит от того, нужно ли изменить или просто просмотреть данные:</span><span class="sxs-lookup"><span data-stu-id="0e68f-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="0e68f-109">Если вам нужно прокрутить набор результатов, но не [](forward-only-cursors.md) изменять данные, используйте курсор "только вперед" или "статический". [](static-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="0e68f-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="0e68f-110">Если у вас большой набор результатов и вам нужно выбрать всего несколько строк, используйте курсор [набора](keyset-cursors.md) клавиш.</span><span class="sxs-lookup"><span data-stu-id="0e68f-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="0e68f-111">Если вы хотите синхронизировать набор результатов с недавними добавлениями, изменениями и удалениями всех пользователей одновременно, используйте [динамический](dynamic-cursors.md) курсор.</span><span class="sxs-lookup"><span data-stu-id="0e68f-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="0e68f-112">Хотя каждый тип курсора кажется отдельным, помните, что эти типы курсоров не так сильно отличаются, как просто результат перекрывающихся характеристик и параметров.</span><span class="sxs-lookup"><span data-stu-id="0e68f-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

