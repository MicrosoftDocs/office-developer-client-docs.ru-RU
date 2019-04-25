---
title: Инструкция CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295368"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="811f2-102">Инструкция CREATE VIEW (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="811f2-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="811f2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="811f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="811f2-104">Создает представление.</span><span class="sxs-lookup"><span data-stu-id="811f2-104">Creates a new folder.</span></span>

> [!NOTE]
> <span data-ttu-id="811f2-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE VIEW или любой другой инструкции DDL с базами данных не на основе ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="811f2-105">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="811f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="811f2-106">Syntax</span></span>

<span data-ttu-id="811f2-107">CREATE VIEW *представление* \[(*поле1*\[, *поле2*\[, …\]\])\] AS *инструкция_SELECT*</span><span class="sxs-lookup"><span data-stu-id="811f2-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="811f2-108">Инструкция CREATE VIEW включает приведенные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="811f2-108">The CREATE PROCEDURE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="811f2-109">Часть</span><span class="sxs-lookup"><span data-stu-id="811f2-109">Part</span></span></p></th>
<th><p><span data-ttu-id="811f2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="811f2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="811f2-111"><em>представление</em></span><span class="sxs-lookup"><span data-stu-id="811f2-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="811f2-112">Имя создаваемого представления.</span><span class="sxs-lookup"><span data-stu-id="811f2-112">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="811f2-113"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="811f2-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="811f2-114">Имена соответствующих полей, заданных в элементе <em>инструкция_SELECT</em>.</span><span class="sxs-lookup"><span data-stu-id="811f2-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="811f2-115"><em>инструкция_SELECT</em></span><span class="sxs-lookup"><span data-stu-id="811f2-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="811f2-116">Инструкция SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="811f2-116">A SQL SELECT statement.</span></span> <span data-ttu-id="811f2-117">Дополнительные сведения см. в статье <a href="select-statement-microsoft-access-sql.md">Инструкция SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="811f2-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="811f2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="811f2-118">Remarks</span></span>

<span data-ttu-id="811f2-119">Инструкция SELECT, определяющая представление, не может быть инструкцией [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="811f2-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="811f2-120">Инструкция SELECT, определяющая представление, не должна содержать параметров.</span><span class="sxs-lookup"><span data-stu-id="811f2-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="811f2-121">Имя представления не может совпадать с именем существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="811f2-121">A procedure name cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="811f2-122">Если запрос, определенный инструкцией SELECT, является обновляемым, представление также может обновляться.</span><span class="sxs-lookup"><span data-stu-id="811f2-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="811f2-123">В противном случае оно предназначено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="811f2-123">Otherwise, the classic view is rendered.</span></span>

<span data-ttu-id="811f2-124">Если любые два поля в запросе, определенном инструкцией SELECT, имеют одинаковые имена, определение представления должно содержать список уникальных имен для каждого поля в запросе.</span><span class="sxs-lookup"><span data-stu-id="811f2-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

