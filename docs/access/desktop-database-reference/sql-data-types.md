---
title: Типы данных SQL (Справочник по для настольных баз данных Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ef5a794014f1397202483e008d164cb5de0b5179
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997814"
---
# <a name="sql-data-types"></a><span data-ttu-id="f4d9b-102">Типы данных SQL</span><span class="sxs-lookup"><span data-stu-id="f4d9b-102">SQL data types</span></span>

<span data-ttu-id="f4d9b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4d9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4d9b-104">Типы данных SQL ядра базы данных Microsoft Access состоят из 13 основных типов данных определяется базы данных Microsoft Jet и нескольких допустимых синонимов, распознанные для этих типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="f4d9b-105">В следующей таблице перечислены основные типы данных.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-105">The following table lists the primary data types.</span></span> <span data-ttu-id="f4d9b-106">Синонимы, определяются в [Microsoft Access базы данных модуля SQL зарезервированные слова](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="f4d9b-106">The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4d9b-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f4d9b-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="f4d9b-108">Размер хранилища</span><span class="sxs-lookup"><span data-stu-id="f4d9b-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="f4d9b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f4d9b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-110">ДВОИЧНЫЙ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-111">1 байт на символ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-112">Любой тип данных может храниться в поле этого типа.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-112">Any type of data may be stored in a field of this type.</span></span> <span data-ttu-id="f4d9b-113">Выполняется без преобразования данных (например, текст).</span><span class="sxs-lookup"><span data-stu-id="f4d9b-113">No translation of the data (for example, to text) is made.</span></span> <span data-ttu-id="f4d9b-114">Способ ввода данных в бинарное поле определяет, как оно будет отображаться в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-114">How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-115">БИТ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-116">1 байт</span><span class="sxs-lookup"><span data-stu-id="f4d9b-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-117">Да и нет значения и поля, которые содержат только один из двух значений.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="f4d9b-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-119">1 байт</span><span class="sxs-lookup"><span data-stu-id="f4d9b-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-120">Целое число от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-121">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-122">8 байтов</span><span class="sxs-lookup"><span data-stu-id="f4d9b-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-123">Масштабируемое целое число между – 922,337,203,685,477.5808 и 922337203685477,5807.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-124">Даты и времени (см.)</span><span class="sxs-lookup"><span data-stu-id="f4d9b-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-125">8 байтов</span><span class="sxs-lookup"><span data-stu-id="f4d9b-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-126">Значение даты или времени между лет 100 до 9999.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="f4d9b-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-128">128 бит</span><span class="sxs-lookup"><span data-stu-id="f4d9b-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-129">Уникальный идентификационный номер, используемый с удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-130">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-131">4 байта</span><span class="sxs-lookup"><span data-stu-id="f4d9b-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-132">Значение с плавающей запятой одиночной точности с в диапазоне от-3, 402823E38 до-1, 401298E-45 для отрицательных значений, от 1, 401298E-45 до 3, 402823E38 для положительных значений и 0.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f4d9b-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-134">8 байтов</span><span class="sxs-lookup"><span data-stu-id="f4d9b-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-135">Значение с плавающей запятой двойной точности в диапазоне от-1, 79769313486232E308 до-4, 94065645841247E-324 для отрицательных значений, от 4, 94065645841247E-324 до 1, 79769313486232E308 для положительных значений и 0.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="f4d9b-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-137">2 байта</span><span class="sxs-lookup"><span data-stu-id="f4d9b-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-138">Короткое целое число от-32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-138">A short integer between – 32,768 and 32,767.</span></span> <span data-ttu-id="f4d9b-139">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="f4d9b-139">(See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-140">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="f4d9b-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-141">4 байта</span><span class="sxs-lookup"><span data-stu-id="f4d9b-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-142">Длинное целое число от-2 147 483 648 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-142">A long integer between – 2,147,483,648 and 2,147,483,647.</span></span> <span data-ttu-id="f4d9b-143">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="f4d9b-143">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="f4d9b-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-145">17 байт</span><span class="sxs-lookup"><span data-stu-id="f4d9b-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-146">Точный числовой тип, в котором содержатся значения от 1028-1 до - 1028-1.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-146">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1.</span></span> <span data-ttu-id="f4d9b-147">Можно определить как точность (1-28), так и масштаб (точность определена как 0).</span><span class="sxs-lookup"><span data-stu-id="f4d9b-147">You can define both precision (1 - 28) and scale (0 - defined precision).</span></span> <span data-ttu-id="f4d9b-148">По умолчанию точности и масштаба, 18 и 0 соответственно.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-148">The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-149">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-150">2 байта на символ (см)</span><span class="sxs-lookup"><span data-stu-id="f4d9b-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-151">От нуля до 2,14 гигабайта.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4d9b-152">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-153">При необходимости</span><span class="sxs-lookup"><span data-stu-id="f4d9b-153">As required</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-154">От нуля до 2,14 гигабайта.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-154">Zero to a maximum of 2.14 gigabytes.</span></span> <span data-ttu-id="f4d9b-155">Используется для объектов OLE.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-155">Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4d9b-156">СИМВОЛ</span><span class="sxs-lookup"><span data-stu-id="f4d9b-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-157">2 байта на символ (см)</span><span class="sxs-lookup"><span data-stu-id="f4d9b-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="f4d9b-158">Ноль до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="f4d9b-159">Начальное значение и приращение может быть изменено с помощью [инструкции ALTER TABLE](alter-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="f4d9b-159">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md).</span></span> <span data-ttu-id="f4d9b-160">Новые строки вставляется в таблицу будут иметь значения на основе нового начального значения и значения приращения, которые автоматически создаются для столбца.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-160">New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column.</span></span> <span data-ttu-id="f4d9b-161">Если новые начальное число и шаг может дать значения, которые соответствуют значениям, созданным на основе предыдущего начального значения и порядкового номера, дубликаты будут создаваться.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-161">If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated.</span></span> <span data-ttu-id="f4d9b-162">Если столбец первичного ключа, добавление новых строк может привести к ошибкам при создании повторяющихся значений.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-162">If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="f4d9b-163">Чтобы найти последнее значение, использованное для столбца с автоматическим шагом, можно использовать следующий оператор: SELECT @@IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-163">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY.</span></span> <span data-ttu-id="f4d9b-164">Не удается задать имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-164">You cannot specify a table name.</span></span> <span data-ttu-id="f4d9b-165">Возвращаемое значение из последней таблицы, содержащий столбец автоматическое увеличение, который был обновлен.</span><span class="sxs-lookup"><span data-stu-id="f4d9b-165">The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
