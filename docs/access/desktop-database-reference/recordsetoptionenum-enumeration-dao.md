---
title: RecordsetOptionEnum Enumeration (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480224"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="5da16-102">RecordsetOptionEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="5da16-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="5da16-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5da16-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5da16-104">Используется с методом **OpenRecordset** , чтобы указать характеристики объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5da16-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5da16-105">Имя</span><span class="sxs-lookup"><span data-stu-id="5da16-105">Name</span></span></p></th>
<th><p><span data-ttu-id="5da16-106">Значение</span><span class="sxs-lookup"><span data-stu-id="5da16-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5da16-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5da16-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5da16-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="5da16-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="5da16-109">8</span><span class="sxs-lookup"><span data-stu-id="5da16-109">8</span></span></p></td>
<td><p><span data-ttu-id="5da16-110">Позволяет пользователям добавлять новые записи динамический набор, но не позволяет пользователю читать существующие записи.</span><span class="sxs-lookup"><span data-stu-id="5da16-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="5da16-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="5da16-112">32</span><span class="sxs-lookup"><span data-stu-id="5da16-112">32</span></span></p></td>
<td><p><span data-ttu-id="5da16-113">Применяет обновления только для тех полях, которые не влияет на другие записи в динамический набор (динамический набор - и типа только).</span><span class="sxs-lookup"><span data-stu-id="5da16-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da16-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="5da16-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="5da16-115">2</span><span class="sxs-lookup"><span data-stu-id="5da16-115">2</span></span></p></td>
<td><p><span data-ttu-id="5da16-116">Чтение записей набора записей (только типа таблица) не позволяет другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="5da16-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="5da16-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="5da16-118">1</span><span class="sxs-lookup"><span data-stu-id="5da16-118">1</span></span></p></td>
<td><p><span data-ttu-id="5da16-119">Пользователям запрещается изменение записей набора записей.</span><span class="sxs-lookup"><span data-stu-id="5da16-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da16-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="5da16-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="5da16-121">2048</span><span class="sxs-lookup"><span data-stu-id="5da16-121">2048</span></span></p></td>
<td><p><span data-ttu-id="5da16-122">Выполняет запрос без первого вызова функции SQLPrepare ODBC.</span><span class="sxs-lookup"><span data-stu-id="5da16-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="5da16-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="5da16-124">128</span><span class="sxs-lookup"><span data-stu-id="5da16-124">128</span></span></p></td>
<td><p><span data-ttu-id="5da16-125">Откат обновления при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="5da16-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da16-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="5da16-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="5da16-127">256</span><span class="sxs-lookup"><span data-stu-id="5da16-127">256</span></span></p></td>
<td><p><span data-ttu-id="5da16-128">Создает прокрутки, однонаправленные моментальный снимок тип набора записей (только типа моментальный снимок).</span><span class="sxs-lookup"><span data-stu-id="5da16-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="5da16-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="5da16-130">16</span><span class="sxs-lookup"><span data-stu-id="5da16-130">16</span></span></p></td>
<td><p><span data-ttu-id="5da16-131">Применяет обновления всех полей динамический набор даже в том случае, если другие записи, затронутых (динамический набор - и типа только).</span><span class="sxs-lookup"><span data-stu-id="5da16-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da16-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="5da16-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5da16-133">4</span><span class="sxs-lookup"><span data-stu-id="5da16-133">4</span></span></p></td>
<td><p><span data-ttu-id="5da16-134">Открывается записей с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5da16-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="5da16-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="5da16-136">1024</span><span class="sxs-lookup"><span data-stu-id="5da16-136">1024</span></span></p></td>
<td><p><span data-ttu-id="5da16-137">Выполняет асинхронный запрос.</span><span class="sxs-lookup"><span data-stu-id="5da16-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da16-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="5da16-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="5da16-139">512</span><span class="sxs-lookup"><span data-stu-id="5da16-139">512</span></span></p></td>
<td><p><span data-ttu-id="5da16-140">Создает ошибку времени выполнения, если другой пользователь изменение данных редактирования (добавляющий только).</span><span class="sxs-lookup"><span data-stu-id="5da16-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da16-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="5da16-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="5da16-142">64</span><span class="sxs-lookup"><span data-stu-id="5da16-142">64</span></span></p></td>
<td><p><span data-ttu-id="5da16-143">Отправляет инструкции SQL в базе данных ODBC (только типа моментальный снимок).</span><span class="sxs-lookup"><span data-stu-id="5da16-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

