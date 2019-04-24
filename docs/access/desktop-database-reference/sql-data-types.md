---
title: Типы данных SQL (справочник по базам данных Access на компьютере)
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
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308584"
---
# <a name="sql-data-types"></a><span data-ttu-id="d8943-102">Типы данных SQL</span><span class="sxs-lookup"><span data-stu-id="d8943-102">SQL data types</span></span>

<span data-ttu-id="d8943-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8943-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8943-104">Типы данных SQL ядра СУБД Microsoft Access состоят из 13 первичных типов данных, определяемых обработчиком баз данных Microsoft Jet и несколькими допустимыми синонимами, подходящими для этих типов данных.</span><span class="sxs-lookup"><span data-stu-id="d8943-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="d8943-105">В приведенной ниже таблице перечислены первичные типы данных.</span><span class="sxs-lookup"><span data-stu-id="d8943-105">The following table lists the primary data types.</span></span> <span data-ttu-id="d8943-106">Синонимы определены в [Зарезервированных словах SQL ядра СУБД Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="d8943-106">The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8943-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d8943-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="d8943-108">Размер хранилища</span><span class="sxs-lookup"><span data-stu-id="d8943-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="d8943-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8943-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8943-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="d8943-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="d8943-111">1 байт на каждый символ</span><span class="sxs-lookup"><span data-stu-id="d8943-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="d8943-112">В поле этого типа может храниться любой тип данных.</span><span class="sxs-lookup"><span data-stu-id="d8943-112">Any type of data may be stored in a field of this type.</span></span> <span data-ttu-id="d8943-113">Нет перевода данных (например, в текст).</span><span class="sxs-lookup"><span data-stu-id="d8943-113">No translation of the data (for example, to text) is made.</span></span> <span data-ttu-id="d8943-114">То, как данные входят в двоичное поле, определяет, как они будут выглядеть в качестве выходных.</span><span class="sxs-lookup"><span data-stu-id="d8943-114">How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-115">BIT</span><span class="sxs-lookup"><span data-stu-id="d8943-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="d8943-116">1 байт</span><span class="sxs-lookup"><span data-stu-id="d8943-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="d8943-117">Значения "Да" и "Нет" и поля, содержащие только одно из двух значений.</span><span class="sxs-lookup"><span data-stu-id="d8943-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="d8943-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="d8943-119">1 байт</span><span class="sxs-lookup"><span data-stu-id="d8943-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="d8943-120">Целое число от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="d8943-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="d8943-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="d8943-122">8 байтов</span><span class="sxs-lookup"><span data-stu-id="d8943-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-123">Масштаб целого числа от 922 337 203 685 477,5808 до 922 337 203 685 477,5807.</span><span class="sxs-lookup"><span data-stu-id="d8943-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-124">DATETIME (см. DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="d8943-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="d8943-125">8 байтов</span><span class="sxs-lookup"><span data-stu-id="d8943-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-126">Значение даты и времени между годами от 100 до 9999.</span><span class="sxs-lookup"><span data-stu-id="d8943-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="d8943-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="d8943-128">128 битов</span><span class="sxs-lookup"><span data-stu-id="d8943-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="d8943-129">Уникальный идентификационный номер, используемый с удаленными вызовами процедур.</span><span class="sxs-lookup"><span data-stu-id="d8943-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-130">REAL</span><span class="sxs-lookup"><span data-stu-id="d8943-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="d8943-131">4 байта</span><span class="sxs-lookup"><span data-stu-id="d8943-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-132">Значение с плавающей запятой одинарной точности с диапазоном от –3,402823E38 до –1,401298E-45 для отрицательных значений, от 1,401298E-45 до 3,402823E38 для положительных значений, а также 0.</span><span class="sxs-lookup"><span data-stu-id="d8943-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d8943-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="d8943-134">8 байтов</span><span class="sxs-lookup"><span data-stu-id="d8943-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-135">Значение с плавающей запятой двойной точности с диапазоном от –1,79769313486232E308 до –4,94065645841247E-324 для отрицательных значений, от 4,94065645841247E-324 до 1,79769313486232E308 для положительных значений, а также 0.</span><span class="sxs-lookup"><span data-stu-id="d8943-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="d8943-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="d8943-137">2 байта</span><span class="sxs-lookup"><span data-stu-id="d8943-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-138">Короткое целое число в диапазоне от –32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="d8943-138">A short integer between – 32,768 and 32,767.</span></span> <span data-ttu-id="d8943-139">(См. "Примечания")</span><span class="sxs-lookup"><span data-stu-id="d8943-139">(See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="d8943-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="d8943-141">4 байта</span><span class="sxs-lookup"><span data-stu-id="d8943-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-142">Длинное целое число в диапазоне от –2 147 483 648 до 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="d8943-142">A long integer between – 2,147,483,648 and 2,147,483,647.</span></span> <span data-ttu-id="d8943-143">(См. "Примечания")</span><span class="sxs-lookup"><span data-stu-id="d8943-143">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="d8943-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="d8943-145">17 байтов</span><span class="sxs-lookup"><span data-stu-id="d8943-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="d8943-146">Тип точных числовых данных, содержащих значения от 1028 – 1 до –1028 – 1.</span><span class="sxs-lookup"><span data-stu-id="d8943-146">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1.</span></span> <span data-ttu-id="d8943-147">Можно задать два параметра: precision (в диапазоне от 1 до 28) и scale (в диапазоне от 0 до заданного значения параметра precision).</span><span class="sxs-lookup"><span data-stu-id="d8943-147">You can define both precision (1 - 28) and scale (0 - defined precision).</span></span> <span data-ttu-id="d8943-148">По умолчанию значения параметров precision и scale равны 18 и 0, соответственно.</span><span class="sxs-lookup"><span data-stu-id="d8943-148">The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="d8943-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="d8943-150">2 байта на каждый символ (см. "Примечания")</span><span class="sxs-lookup"><span data-stu-id="d8943-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="d8943-151">Значение от 0 до 2,14 гигабайт.</span><span class="sxs-lookup"><span data-stu-id="d8943-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8943-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="d8943-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="d8943-153">В соответствии с требованием</span><span class="sxs-lookup"><span data-stu-id="d8943-153">As required</span></span></p></td>
<td><p><span data-ttu-id="d8943-154">Значение от 0 до 2,14 гигабайт.</span><span class="sxs-lookup"><span data-stu-id="d8943-154">Zero to a maximum of 2.14 gigabytes.</span></span> <span data-ttu-id="d8943-155">Используется для объектов OLE.</span><span class="sxs-lookup"><span data-stu-id="d8943-155">Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8943-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="d8943-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="d8943-157">2 байта на каждый символ (см. "Примечания")</span><span class="sxs-lookup"><span data-stu-id="d8943-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="d8943-158">Значение от 0 до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="d8943-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="d8943-159">Начальное значение и шаг приращения можно изменить, используя [инструкцию ALTER TABLE](alter-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="d8943-159">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md).</span></span> <span data-ttu-id="d8943-160">Добавленные в таблицу строки будут содержать значения, основанные на новом начальном значении и шаге приращения, которые автоматически создаются для столбца.</span><span class="sxs-lookup"><span data-stu-id="d8943-160">New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column.</span></span> <span data-ttu-id="d8943-161">Если новое начальное значение и шаг приращения меньше значений, которые соответствуют созданным на основании предыдущего начального значения и шага приращения, создаются повторяющиеся значения.</span><span class="sxs-lookup"><span data-stu-id="d8943-161">If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated.</span></span> <span data-ttu-id="d8943-162">Если столбец представляет собой первичный ключ, то вставка новых строк может привести к ошибкам при создании повторяющихся значений.</span><span class="sxs-lookup"><span data-stu-id="d8943-162">If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="d8943-163">Для получения последнего значения, которое использовалось для столбца автоприращения, можно использовать инструкцию SELECT @@IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="d8943-163">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY.</span></span> <span data-ttu-id="d8943-164">Невозможно задать имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="d8943-164">You cannot specify a table name.</span></span> <span data-ttu-id="d8943-165">Возвращаемое значение — значение из последней таблицы, содержащей столбец автоприращения, которая была обновлена.</span><span class="sxs-lookup"><span data-stu-id="d8943-165">The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
