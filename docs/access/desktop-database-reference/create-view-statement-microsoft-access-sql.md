---
title: Инструкция CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f1d13cef4551975dc316b2fbedf2388028956fb3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862907"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="17b82-102">Инструкция CREATE VIEW (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="17b82-102">CREATE VIEW statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="17b82-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17b82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17b82-104">Создание нового представления.</span><span class="sxs-lookup"><span data-stu-id="17b82-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="17b82-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE VIEW или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="17b82-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b82-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17b82-106">Syntax</span></span>

<span data-ttu-id="17b82-107">Создание ПРЕДСТАВЛЕНИЯ *представление* \[(*field1*\[, *поле2*\[,... \] \])\] Как *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="17b82-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="17b82-108">Инструкция CREATE VIEW состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="17b82-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17b82-109">Часть</span><span class="sxs-lookup"><span data-stu-id="17b82-109">Part</span></span></p></th>
<th><p><span data-ttu-id="17b82-110">Описание</span><span class="sxs-lookup"><span data-stu-id="17b82-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17b82-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="17b82-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="17b82-112">Имя представления будет создан.</span><span class="sxs-lookup"><span data-stu-id="17b82-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b82-113"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="17b82-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="17b82-114">Имя поля или полей для соответствующих полей, определенных в <em>selectstatement</em>.</span><span class="sxs-lookup"><span data-stu-id="17b82-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b82-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="17b82-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="17b82-116">Инструкция SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="17b82-116">A SQL SELECT statement.</span></span> <span data-ttu-id="17b82-117">Дополнительные сведения см в <a href="select-statement-microsoft-access-sql.md">оператор SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="17b82-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="17b82-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="17b82-118">Remarks</span></span>

<span data-ttu-id="17b82-119">ВЫБЕРИТЕ оператор, определяющий представление, не может быть инструкции [SELECT INTO](select-into-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="17b82-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="17b82-120">ВЫБЕРИТЕ оператор, определяющий представление, не может содержать каких-либо параметров.</span><span class="sxs-lookup"><span data-stu-id="17b82-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="17b82-121">Имя представления не может быть имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="17b82-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="17b82-122">Если запрос, определенные в инструкции SELECT является обновляемым, представление также может обновляться.</span><span class="sxs-lookup"><span data-stu-id="17b82-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="17b82-123">В противном случае представление доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="17b82-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="17b82-124">Если любые два поля в запросе, определенные в инструкции SELECT имеет то же имя, определение представления должно содержать список полей, определяющее уникальные имена для каждого поля в запросе.</span><span class="sxs-lookup"><span data-stu-id="17b82-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

