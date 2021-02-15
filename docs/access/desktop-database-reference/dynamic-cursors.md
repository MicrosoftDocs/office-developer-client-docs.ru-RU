---
title: Динамические курсоры (справочник по базе данных Access для настольных ПК)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293639"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="84abc-102">Динамические курсоры</span><span class="sxs-lookup"><span data-stu-id="84abc-102">Dynamic cursors</span></span>


<span data-ttu-id="84abc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84abc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84abc-104">Динамические курсоры обнаруживают все изменения, внесенные в строки в наборе результатов, независимо от того, происходят ли изменения из курсора или других пользователей за пределами курсора.</span><span class="sxs-lookup"><span data-stu-id="84abc-104">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor.</span></span> <span data-ttu-id="84abc-105">Все заявления о вставке, обновлении и удалении, сделанные всеми пользователями, видны через курсор.</span><span class="sxs-lookup"><span data-stu-id="84abc-105">All insert, update, and delete statements made by all users are visible through the cursor.</span></span> <span data-ttu-id="84abc-106">Динамический курсор может обнаруживать любые изменения, внесенные в строки, порядок и значения в наборе результатов после открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="84abc-106">The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened.</span></span> <span data-ttu-id="84abc-107">Обновления, сделанные вне курсора, не видны, пока они не будут зафиксированы (если только для уровня изоляции транзакций курсора не установлено "незафиксировать").</span><span class="sxs-lookup"><span data-stu-id="84abc-107">Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="84abc-108">Например, предположим, что динамический курсор извлекает две строки и другое приложение, а затем обновляет одну из них и удаляет другую.</span><span class="sxs-lookup"><span data-stu-id="84abc-108">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other.</span></span> <span data-ttu-id="84abc-109">Если динамический курсор затем извлекает эти строки, он не найдет удаленную строку, но отобразит новые значения для обновленной строки.</span><span class="sxs-lookup"><span data-stu-id="84abc-109">If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="84abc-110">Динамический курсор является хорошим выбором, если приложение должно обнаружить все одновременно сделанные другими пользователями обновления.</span><span class="sxs-lookup"><span data-stu-id="84abc-110">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users.</span></span> <span data-ttu-id="84abc-111">Используйте **adOpenDynamic** **CursorTypeEnum,** чтобы указать, что вы хотите использовать динамический курсор в ADO.</span><span class="sxs-lookup"><span data-stu-id="84abc-111">Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="84abc-112">[Курсоры только для переад.](forward-only-cursors.md)  |  [Статические курсоры](static-cursors.md)  |  [Курсоры keyset](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="84abc-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

