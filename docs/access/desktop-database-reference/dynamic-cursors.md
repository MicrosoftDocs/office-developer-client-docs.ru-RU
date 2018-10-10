---
title: Динамические курсоры (Справочник по для настольных баз данных Access)
TOCTitle: Dynamic Cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c324923f0e702ad59ac120ea5de2eebcccd260e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479759"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="fef04-102">Dynamic Cursors</span><span class="sxs-lookup"><span data-stu-id="fef04-102">Dynamic Cursors</span></span>


<span data-ttu-id="fef04-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fef04-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fef04-104">Динамические курсоры обнаруживает все изменения, внесенные для строк в результирующем наборе, независимо от того, ли изменениях из внутри курсора или другими пользователями за пределами курсора.</span><span class="sxs-lookup"><span data-stu-id="fef04-104">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor.</span></span> <span data-ttu-id="fef04-105">Все insert, update и delete операторов всех пользователей видны посредством курсора.</span><span class="sxs-lookup"><span data-stu-id="fef04-105">All insert, update, and delete statements made by all users are visible through the cursor.</span></span> <span data-ttu-id="fef04-106">Динамический курсор может обнаруживать изменения, внесенные строк, порядок и значения в результирующем наборе, после открытия курсора.</span><span class="sxs-lookup"><span data-stu-id="fef04-106">The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened.</span></span> <span data-ttu-id="fef04-107">Обновления, сделанные вне курсора не видны до момента фиксации (если уровень изоляции транзакций курсора не задано значение «незафиксированные»).</span><span class="sxs-lookup"><span data-stu-id="fef04-107">Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="fef04-108">Предположим, например, динамический курсор извлекает две строки и другого приложения и обновляет один из этих строк и удаляет другое.</span><span class="sxs-lookup"><span data-stu-id="fef04-108">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other.</span></span> <span data-ttu-id="fef04-109">Если динамический курсор затем извлекает эти строки, не найдете удаленной строки, но он будет отображать нового значения для обновленные строки.</span><span class="sxs-lookup"><span data-stu-id="fef04-109">If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="fef04-110">Динамический курсор является хорошим выбором, если приложение должно определять всех одновременных обновлений, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="fef04-110">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users.</span></span> <span data-ttu-id="fef04-111">Чтобы указать, что вы хотите использовать динамический курсор в ADO используйте **adOpenDynamic** **CursorTypeEnum** .</span><span class="sxs-lookup"><span data-stu-id="fef04-111">Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="fef04-112">[Курсоров](forward-only-cursors.md) | [статические курсоры](static-cursors.md) | [курсоры ключей](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="fef04-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

