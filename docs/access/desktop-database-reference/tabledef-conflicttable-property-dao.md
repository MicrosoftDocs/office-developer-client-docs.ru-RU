---
title: Свойство TableDef. Конфликттабле (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308430"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="6d974-102">Свойство TableDef. Конфликттабле (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d974-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="6d974-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d974-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d974-104">Возвращает имя таблицы конфликтов, содержащей записи базы данных, которые конфликтуют при синхронизации двух реплик (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6d974-104">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6d974-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="6d974-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d974-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d974-106">Syntax</span></span>

<span data-ttu-id="6d974-107">*Expression* . Конфликттабле</span><span class="sxs-lookup"><span data-stu-id="6d974-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="6d974-108">*Expression (выражение* ) Выражение, возвращающее объект **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="6d974-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d974-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d974-109">Remarks</span></span>

<span data-ttu-id="6d974-110">Возвращаемое значение — это **строковый** тип данных, который является строкой нулевой длины (""), если нет таблицы конфликтов или база данных не является репликой.</span><span class="sxs-lookup"><span data-stu-id="6d974-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="6d974-111">Если два пользователя в двух отдельных репликах изменяют одну и ту же запись в базе данных, изменения, внесенные одним пользователем, не будут применены к другой реплике.</span><span class="sxs-lookup"><span data-stu-id="6d974-111">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica.</span></span> <span data-ttu-id="6d974-112">Следовательно, пользователь с неудачным изменением должен разрешить конфликты.</span><span class="sxs-lookup"><span data-stu-id="6d974-112">Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="6d974-113">Конфликты возникают на уровне записей, а не между полями.</span><span class="sxs-lookup"><span data-stu-id="6d974-113">Conflicts occur at the record level, not between fields.</span></span> <span data-ttu-id="6d974-114">Например, если один пользователь изменяет поле адрес, а другое обновляет поле Телефон в той же записи, одно изменение отклоняется.</span><span class="sxs-lookup"><span data-stu-id="6d974-114">For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected.</span></span> <span data-ttu-id="6d974-115">Так как конфликты происходят на уровне записей, отклонения происходят, несмотря на то, что в случае успешного изменения и отклоненных изменений маловероятно, что конфликт данных является истинным.</span><span class="sxs-lookup"><span data-stu-id="6d974-115">Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="6d974-116">Механизм синхронизации обрабатывает конфликты записей, создавая таблицы конфликтов, которые содержат сведения, которые были размещены в таблице, если изменение было успешным.</span><span class="sxs-lookup"><span data-stu-id="6d974-116">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful.</span></span> <span data-ttu-id="6d974-117">Вы можете проверить эти таблицы конфликтов и проработать их по строкам по строкам, исправив все подходящие.</span><span class="sxs-lookup"><span data-stu-id="6d974-117">You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="6d974-118">Все таблицы конфликтов называются конфликтами таблиц\_, где Table — это исходное имя таблицы, усеченное до максимальной длины имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="6d974-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

