---
title: DataTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7d1cbc0964c4e980c1dd5216431c5efd0c467dc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878264"
---
# <a name="datatypeenum"></a><span data-ttu-id="568f8-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="568f8-102">DataTypeEnum</span></span>

<span data-ttu-id="568f8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="568f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="568f8-104">Указывает тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="568f8-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="568f8-105">В скобки в столбце Описание в следующей таблице показан соответствующий индикатор типа OLE DB.</span><span class="sxs-lookup"><span data-stu-id="568f8-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="568f8-106">Дополнительные сведения о типах данных OLE DB видеть главе 13 и приложение A *Справочник программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="568f8-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="568f8-107">Константа</span><span class="sxs-lookup"><span data-stu-id="568f8-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="568f8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="568f8-108">Value</span></span></p></th>
<th><p><span data-ttu-id="568f8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="568f8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="568f8-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="568f8-110"><strong>AdArray</span></span><br /><span data-ttu-id="568f8-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="568f8-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="568f8-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="568f8-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="568f8-113">Значение флага, всегда вместе с другой тип данных константа, которая указывает массив, другой тип данных.</span><span class="sxs-lookup"><span data-stu-id="568f8-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-115">20</span><span class="sxs-lookup"><span data-stu-id="568f8-115">20</span></span></p></td>
<td><p><span data-ttu-id="568f8-116">Указывает целое число 8 байт со знаком (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="568f8-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-118">128</span><span class="sxs-lookup"><span data-stu-id="568f8-118">128</span></span></p></td>
<td><p><span data-ttu-id="568f8-119">Указывает двоичное значение (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="568f8-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-121">11</span><span class="sxs-lookup"><span data-stu-id="568f8-121">11</span></span></p></td>
<td><p><span data-ttu-id="568f8-122">Указывает логическое значение (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="568f8-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-124">8</span><span class="sxs-lookup"><span data-stu-id="568f8-124">8</span></span></p></td>
<td><p><span data-ttu-id="568f8-125">Указывает строку символом null знаков (Юникод) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="568f8-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-127">136</span><span class="sxs-lookup"><span data-stu-id="568f8-127">136</span></span></p></td>
<td><p><span data-ttu-id="568f8-128">Указывает, Глава 4 байтовое значение, указывающее строки в дочерних строк (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="568f8-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-130">129</span><span class="sxs-lookup"><span data-stu-id="568f8-130">129</span></span></p></td>
<td><p><span data-ttu-id="568f8-131">Указывает значение string (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="568f8-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-133">6</span><span class="sxs-lookup"><span data-stu-id="568f8-133">6</span></span></p></td>
<td><p><span data-ttu-id="568f8-134">Указывает значение валюты (DBTYPE_CY).</span><span class="sxs-lookup"><span data-stu-id="568f8-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="568f8-135">Валюта является фиксированной числа с четырех цифр справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="568f8-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="568f8-136">Он хранится в 8 байтовое целое число со знаком, масштабируемые с 10 000.</span><span class="sxs-lookup"><span data-stu-id="568f8-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-138">7</span><span class="sxs-lookup"><span data-stu-id="568f8-138">7</span></span></p></td>
<td><p><span data-ttu-id="568f8-139">Указывает значение даты (DBTYPE_DATE).</span><span class="sxs-lookup"><span data-stu-id="568f8-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="568f8-140">Дата сохраняется как значение типа double, всей часть из которых — число дней, прошедших с 30 декабря 1899, а дробная часть из которых — долю дня.</span><span class="sxs-lookup"><span data-stu-id="568f8-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-142">133</span><span class="sxs-lookup"><span data-stu-id="568f8-142">133</span></span></p></td>
<td><p><span data-ttu-id="568f8-143">Указывает значение даты (ГГГГММДД) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="568f8-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-145">134</span><span class="sxs-lookup"><span data-stu-id="568f8-145">134</span></span></p></td>
<td><p><span data-ttu-id="568f8-146">Указывает значение времени (ЧЧММСС) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="568f8-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-148">135</span><span class="sxs-lookup"><span data-stu-id="568f8-148">135</span></span></p></td>
<td><p><span data-ttu-id="568f8-149">Указывает метку даты/времени (ггггммддччммсс плюс дроби в billionths) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="568f8-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-151">14</span><span class="sxs-lookup"><span data-stu-id="568f8-151">14</span></span></p></td>
<td><p><span data-ttu-id="568f8-152">Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="568f8-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-154">5</span><span class="sxs-lookup"><span data-stu-id="568f8-154">5</span></span></p></td>
<td><p><span data-ttu-id="568f8-155">Указывает значение с плавающей запятой двойной точности (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="568f8-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-157">0</span><span class="sxs-lookup"><span data-stu-id="568f8-157">0</span></span></p></td>
<td><p><span data-ttu-id="568f8-158">Не заданы значения (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="568f8-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-160">10</span><span class="sxs-lookup"><span data-stu-id="568f8-160">10</span></span></p></td>
<td><p><span data-ttu-id="568f8-161">Указывает код ошибки 32-разрядная версия (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="568f8-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-163">64</span><span class="sxs-lookup"><span data-stu-id="568f8-163">64</span></span></p></td>
<td><p><span data-ttu-id="568f8-164">Указывает значение 64-разрядная версия, представляющее количество 100 наносекунд интервалов с 1 января 1601 г. (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="568f8-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-166">72</span><span class="sxs-lookup"><span data-stu-id="568f8-166">72</span></span></p></td>
<td><p><span data-ttu-id="568f8-167">Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="568f8-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-169">9</span><span class="sxs-lookup"><span data-stu-id="568f8-169">9</span></span></p></td>
<td><p><span data-ttu-id="568f8-170">Обозначает указатель на интерфейс <strong>IDispatch</strong> на COM-объект (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="568f8-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="568f8-171"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="568f8-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="568f8-172">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="568f8-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-174">3</span><span class="sxs-lookup"><span data-stu-id="568f8-174">3</span></span></p></td>
<td><p><span data-ttu-id="568f8-175">Указывает 4 байта целого числа со знаком (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="568f8-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-177">13</span><span class="sxs-lookup"><span data-stu-id="568f8-177">13</span></span></p></td>
<td><p><span data-ttu-id="568f8-178">Указывает указатель на интерфейс <strong>IUnknown</strong> COM-объект (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="568f8-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="568f8-179"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="568f8-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="568f8-180">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="568f8-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-182">205</span><span class="sxs-lookup"><span data-stu-id="568f8-182">205</span></span></p></td>
<td><p><span data-ttu-id="568f8-183">Указывает Длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="568f8-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-185">201</span><span class="sxs-lookup"><span data-stu-id="568f8-185">201</span></span></p></td>
<td><p><span data-ttu-id="568f8-186">Указывает значение длинной строкой.</span><span class="sxs-lookup"><span data-stu-id="568f8-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-188">203</span><span class="sxs-lookup"><span data-stu-id="568f8-188">203</span></span></p></td>
<td><p><span data-ttu-id="568f8-189">Указывает значение строки Юникод долго символом null.</span><span class="sxs-lookup"><span data-stu-id="568f8-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-191">131</span><span class="sxs-lookup"><span data-stu-id="568f8-191">131</span></span></p></td>
<td><p><span data-ttu-id="568f8-192">Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="568f8-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-194">138</span><span class="sxs-lookup"><span data-stu-id="568f8-194">138</span></span></p></td>
<td><p><span data-ttu-id="568f8-195">Указывает автоматизация PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="568f8-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-197">4</span><span class="sxs-lookup"><span data-stu-id="568f8-197">4</span></span></p></td>
<td><p><span data-ttu-id="568f8-198">Указывает значение с плавающей запятой одиночной точности (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="568f8-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-200">2</span><span class="sxs-lookup"><span data-stu-id="568f8-200">2</span></span></p></td>
<td><p><span data-ttu-id="568f8-201">Указывает двухбайтовые целого числа со знаком (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="568f8-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-203">16</span><span class="sxs-lookup"><span data-stu-id="568f8-203">16</span></span></p></td>
<td><p><span data-ttu-id="568f8-204">Указывает один байт целого числа со знаком (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="568f8-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-206">21</span><span class="sxs-lookup"><span data-stu-id="568f8-206">21</span></span></p></td>
<td><p><span data-ttu-id="568f8-207">Указывает, 8 байтовое целое (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="568f8-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-209">19</span><span class="sxs-lookup"><span data-stu-id="568f8-209">19</span></span></p></td>
<td><p><span data-ttu-id="568f8-210">Указывает, 4 байтовое целое число без знака (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="568f8-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-212">18</span><span class="sxs-lookup"><span data-stu-id="568f8-212">18</span></span></p></td>
<td><p><span data-ttu-id="568f8-213">Указывает, 2 байтовое целое число без знака (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="568f8-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-215">17</span><span class="sxs-lookup"><span data-stu-id="568f8-215">17</span></span></p></td>
<td><p><span data-ttu-id="568f8-216">Указывает один байтовое целое число без знака (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="568f8-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-218">132</span><span class="sxs-lookup"><span data-stu-id="568f8-218">132</span></span></p></td>
<td><p><span data-ttu-id="568f8-219">Указывает, определенные пользователем переменные (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="568f8-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-221">204</span><span class="sxs-lookup"><span data-stu-id="568f8-221">204</span></span></p></td>
<td><p><span data-ttu-id="568f8-222">Указывает двоичное значение (только для<strong>параметра</strong> объект).</span><span class="sxs-lookup"><span data-stu-id="568f8-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-224">200</span><span class="sxs-lookup"><span data-stu-id="568f8-224">200</span></span></p></td>
<td><p><span data-ttu-id="568f8-225">Указывает значение строки.</span><span class="sxs-lookup"><span data-stu-id="568f8-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-227">12</span><span class="sxs-lookup"><span data-stu-id="568f8-227">12</span></span></p></td>
<td><p><span data-ttu-id="568f8-228">Указывает, автоматизации <strong>Variant</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="568f8-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="568f8-229"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="568f8-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="568f8-230">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="568f8-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-232">139</span><span class="sxs-lookup"><span data-stu-id="568f8-232">139</span></span></p></td>
<td><p><span data-ttu-id="568f8-233">Указывает числовое значение (только для<strong>параметра</strong> объект).</span><span class="sxs-lookup"><span data-stu-id="568f8-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-235">202</span><span class="sxs-lookup"><span data-stu-id="568f8-235">202</span></span></p></td>
<td><p><span data-ttu-id="568f8-236">Указывает строку знаков Юникод символом null.</span><span class="sxs-lookup"><span data-stu-id="568f8-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="568f8-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="568f8-238">130</span><span class="sxs-lookup"><span data-stu-id="568f8-238">130</span></span></p></td>
<td><p><span data-ttu-id="568f8-239">Указывает строку знаков Юникод (DBTYPE_WSTR) символом null.</span><span class="sxs-lookup"><span data-stu-id="568f8-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="568f8-240">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="568f8-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="568f8-241">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="568f8-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="568f8-242">Constant</span><span class="sxs-lookup"><span data-stu-id="568f8-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="568f8-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="568f8-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="568f8-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="568f8-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="568f8-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="568f8-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="568f8-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="568f8-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="568f8-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="568f8-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="568f8-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="568f8-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="568f8-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="568f8-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="568f8-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="568f8-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="568f8-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="568f8-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="568f8-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="568f8-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="568f8-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="568f8-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="568f8-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="568f8-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="568f8-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="568f8-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="568f8-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="568f8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="568f8-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="568f8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="568f8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="568f8-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="568f8-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="568f8-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="568f8-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568f8-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568f8-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="568f8-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

