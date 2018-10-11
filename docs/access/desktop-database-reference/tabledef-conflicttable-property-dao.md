---
title: TableDef.ConflictTable Property (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 495930ae659eac588e652caaaf20f0385b383fa8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480295"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="26146-102">TableDef.ConflictTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="26146-102">TableDef.ConflictTable Property (DAO)</span></span>


<span data-ttu-id="26146-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="26146-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="26146-104">Возвращает имя таблицы конфликта, содержащий записи базы данных, которые конфликт во время синхронизации двух реплик (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="26146-104">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only).</span></span> <span data-ttu-id="26146-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="26146-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="26146-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26146-106">Syntax</span></span>

<span data-ttu-id="26146-107">*выражение* . ConflictTable</span><span class="sxs-lookup"><span data-stu-id="26146-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="26146-108">*выражение* Выражение, возвращающее объект **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="26146-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26146-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="26146-109">Remarks</span></span>

<span data-ttu-id="26146-110">Возвращаемое значение имеет тип данных **String** , который является строкой нулевой длины ("») Если нет конфликтов таблицы или базы данных не является репликой.</span><span class="sxs-lookup"><span data-stu-id="26146-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="26146-111">Если двух пользователей в нескольких репликах каждого внести изменения в той же записи в базу данных, изменения, внесенные одним пользователем завершится с ошибкой для применения к другой реплики.</span><span class="sxs-lookup"><span data-stu-id="26146-111">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica.</span></span> <span data-ttu-id="26146-112">Следовательно пользователю с неудачных изменений необходимо разрешить конфликты.</span><span class="sxs-lookup"><span data-stu-id="26146-112">Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="26146-113">Конфликты возникают на уровне записей, не между полями.</span><span class="sxs-lookup"><span data-stu-id="26146-113">Conflicts occur at the record level, not between fields.</span></span> <span data-ttu-id="26146-114">Например если один пользователь изменяет поле адреса и другую обновляет поле телефон в той же записи, затем одно изменение отклоняется.</span><span class="sxs-lookup"><span data-stu-id="26146-114">For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected.</span></span> <span data-ttu-id="26146-115">Так как конфликтов на уровне записей, отклонения возникает несмотря на то, что успешное изменение и отклоненные изменение скорее всего привести значение true, конфликта информации.</span><span class="sxs-lookup"><span data-stu-id="26146-115">Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="26146-116">Механизм синхронизации обрабатывает записи конфликтов путем создания таблицы конфликта, содержащие сведения, которые определены в таблице, если изменения была успешно.</span><span class="sxs-lookup"><span data-stu-id="26146-116">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful.</span></span> <span data-ttu-id="26146-117">Можно проверить эти таблицы конфликтов и работать с ними по строкам, исправление все соответствующие.</span><span class="sxs-lookup"><span data-stu-id="26146-117">You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="26146-118">Все таблицы конфликтов называются таблице\_конфликта, где в таблице — исходное имя таблицы, усекается до максимального таблицы длина имени.</span><span class="sxs-lookup"><span data-stu-id="26146-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

