---
title: Свойство TableDef.ConflictTable (DAO)
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
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="085ff-102">Свойство TableDef.ConflictTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="085ff-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="085ff-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="085ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="085ff-104">Возвращает имя таблицы конфликтов, содержащей записи баз данных, которые конфликтовали во время синхронизации двух реплик (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="085ff-104">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only).</span></span> <span data-ttu-id="085ff-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="085ff-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="085ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="085ff-106">Syntax</span></span>

<span data-ttu-id="085ff-107">*выражения* . ConflictTable</span><span class="sxs-lookup"><span data-stu-id="085ff-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="085ff-108">*выражение* Выражение, возвращаемая **объекту TableDef.**</span><span class="sxs-lookup"><span data-stu-id="085ff-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="085ff-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="085ff-109">Remarks</span></span>

<span data-ttu-id="085ff-110">Возвращаемая величина — это тип данных **String,** который является строкой нулевой длины ("), если нет таблицы конфликтов или база данных не является репликой.</span><span class="sxs-lookup"><span data-stu-id="085ff-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="085ff-111">Если два пользователя по двум отдельным репликам каждый внести изменения в одну запись в базе данных, изменения, внесенные одним пользователем, не будут применены к другой реплике.</span><span class="sxs-lookup"><span data-stu-id="085ff-111">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica.</span></span> <span data-ttu-id="085ff-112">Следовательно, пользователь с неудачным изменением должен разрешить конфликты.</span><span class="sxs-lookup"><span data-stu-id="085ff-112">Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="085ff-113">Конфликты возникают на уровне записи, а не между полями.</span><span class="sxs-lookup"><span data-stu-id="085ff-113">Conflicts occur at the record level, not between fields.</span></span> <span data-ttu-id="085ff-114">Например, если один пользователь изменяет поле Адрес, а другой обновляет Телефон в той же записи, одно изменение отклоняется.</span><span class="sxs-lookup"><span data-stu-id="085ff-114">For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected.</span></span> <span data-ttu-id="085ff-115">Поскольку конфликты происходят на уровне записи, отторжение происходит, несмотря на то, что успешное изменение и отклоненные изменения вряд ли привядут к подлинному конфликту сведений.</span><span class="sxs-lookup"><span data-stu-id="085ff-115">Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="085ff-116">Механизм синхронизации обрабатывает конфликты записей, создавая таблицы конфликтов, содержащие сведения, которые были бы помещены в таблицу, если бы изменение было успешным.</span><span class="sxs-lookup"><span data-stu-id="085ff-116">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful.</span></span> <span data-ttu-id="085ff-117">Вы можете изучить эти таблицы конфликтов и работать через них строки за строкой, исправляя все, что необходимо.</span><span class="sxs-lookup"><span data-stu-id="085ff-117">You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="085ff-118">Все таблицы конфликтов называются конфликтами таблиц, в которых таблица является исходным именем таблицы, усеченной до максимальной \_ длины имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="085ff-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

