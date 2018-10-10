---
title: DataTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b70ad0067083373679286bdb452cb667d3de0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482453"
---
# <a name="datatypeenum"></a><span data-ttu-id="6b129-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="6b129-102">DataTypeEnum</span></span>


<span data-ttu-id="6b129-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b129-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6b129-104">Указывает тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6b129-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="6b129-105">В скобки в столбце Описание в следующей таблице показан соответствующий индикатор типа OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6b129-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="6b129-106">Дополнительные сведения о типах данных OLE DB видеть главе 13 и приложение A *Справочник программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="6b129-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b129-107">Константа</span><span class="sxs-lookup"><span data-stu-id="6b129-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="6b129-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6b129-108">Value</span></span></p></th>
<th><p><span data-ttu-id="6b129-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6b129-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b129-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="6b129-110"><strong>AdArray</span></span><br /><span data-ttu-id="6b129-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="6b129-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="6b129-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="6b129-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="6b129-113">Значение флага, всегда вместе с другой тип данных константа, которая указывает массив, другой тип данных.</span><span class="sxs-lookup"><span data-stu-id="6b129-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-115">20</span><span class="sxs-lookup"><span data-stu-id="6b129-115">20</span></span></p></td>
<td><p><span data-ttu-id="6b129-116">Указывает целое число 8 байт со знаком (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="6b129-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-118">128</span><span class="sxs-lookup"><span data-stu-id="6b129-118">128</span></span></p></td>
<td><p><span data-ttu-id="6b129-119">Указывает двоичное значение (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="6b129-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-121">11</span><span class="sxs-lookup"><span data-stu-id="6b129-121">11</span></span></p></td>
<td><p><span data-ttu-id="6b129-122">Указывает логическое значение (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="6b129-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-124">8</span><span class="sxs-lookup"><span data-stu-id="6b129-124">8</span></span></p></td>
<td><p><span data-ttu-id="6b129-125">Указывает строку символом null знаков (Юникод) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="6b129-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-127">136</span><span class="sxs-lookup"><span data-stu-id="6b129-127">136</span></span></p></td>
<td><p><span data-ttu-id="6b129-128">Указывает, Глава 4 байтовое значение, указывающее строки в дочерних строк (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="6b129-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-130">129</span><span class="sxs-lookup"><span data-stu-id="6b129-130">129</span></span></p></td>
<td><p><span data-ttu-id="6b129-131">Указывает значение string (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="6b129-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-133">6</span><span class="sxs-lookup"><span data-stu-id="6b129-133">6</span></span></p></td>
<td><p><span data-ttu-id="6b129-134">Указывает значение валюты (DBTYPE_CY).</span><span class="sxs-lookup"><span data-stu-id="6b129-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="6b129-135">Валюта является фиксированной числа с четырех цифр справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="6b129-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="6b129-136">Он хранится в 8 байтовое целое число со знаком, масштабируемые с 10 000.</span><span class="sxs-lookup"><span data-stu-id="6b129-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-138">7</span><span class="sxs-lookup"><span data-stu-id="6b129-138">7</span></span></p></td>
<td><p><span data-ttu-id="6b129-139">Указывает значение даты (DBTYPE_DATE).</span><span class="sxs-lookup"><span data-stu-id="6b129-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="6b129-140">Дата сохраняется как значение типа double, всей часть из которых — число дней, прошедших с 30 декабря 1899, а дробная часть из которых — долю дня.</span><span class="sxs-lookup"><span data-stu-id="6b129-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-142">133</span><span class="sxs-lookup"><span data-stu-id="6b129-142">133</span></span></p></td>
<td><p><span data-ttu-id="6b129-143">Указывает значение даты (ГГГГММДД) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="6b129-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-145">134</span><span class="sxs-lookup"><span data-stu-id="6b129-145">134</span></span></p></td>
<td><p><span data-ttu-id="6b129-146">Указывает значение времени (ЧЧММСС) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="6b129-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-148">135</span><span class="sxs-lookup"><span data-stu-id="6b129-148">135</span></span></p></td>
<td><p><span data-ttu-id="6b129-149">Указывает метку даты/времени (ггггммддччммсс плюс дроби в billionths) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="6b129-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-151">14</span><span class="sxs-lookup"><span data-stu-id="6b129-151">14</span></span></p></td>
<td><p><span data-ttu-id="6b129-152">Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="6b129-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-154">5</span><span class="sxs-lookup"><span data-stu-id="6b129-154">5</span></span></p></td>
<td><p><span data-ttu-id="6b129-155">Указывает значение с плавающей запятой двойной точности (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="6b129-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-157">0</span><span class="sxs-lookup"><span data-stu-id="6b129-157">0</span></span></p></td>
<td><p><span data-ttu-id="6b129-158">Не заданы значения (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="6b129-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-160">10</span><span class="sxs-lookup"><span data-stu-id="6b129-160">10</span></span></p></td>
<td><p><span data-ttu-id="6b129-161">Указывает код ошибки 32-разрядная версия (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="6b129-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-163">64</span><span class="sxs-lookup"><span data-stu-id="6b129-163">64</span></span></p></td>
<td><p><span data-ttu-id="6b129-164">Указывает значение 64-разрядная версия, представляющее количество 100 наносекунд интервалов с 1 января 1601 г. (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="6b129-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-166">72</span><span class="sxs-lookup"><span data-stu-id="6b129-166">72</span></span></p></td>
<td><p><span data-ttu-id="6b129-167">Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="6b129-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-169">9</span><span class="sxs-lookup"><span data-stu-id="6b129-169">9</span></span></p></td>
<td><p><span data-ttu-id="6b129-170">Обозначает указатель на интерфейс <strong>IDispatch</strong> на COM-объект (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="6b129-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6b129-171">Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="6b129-171">This data type is currently not supported by ADO.</span></span> <span data-ttu-id="6b129-172">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="6b129-172">Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-174">3</span><span class="sxs-lookup"><span data-stu-id="6b129-174">3</span></span></p></td>
<td><p><span data-ttu-id="6b129-175">Указывает 4 байта целого числа со знаком (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="6b129-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-177">13</span><span class="sxs-lookup"><span data-stu-id="6b129-177">13</span></span></p></td>
<td><p><span data-ttu-id="6b129-178">Указывает указатель на интерфейс <strong>IUnknown</strong> COM-объект (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="6b129-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6b129-179">Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="6b129-179">This data type is currently not supported by ADO.</span></span> <span data-ttu-id="6b129-180">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="6b129-180">Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-182">205</span><span class="sxs-lookup"><span data-stu-id="6b129-182">205</span></span></p></td>
<td><p><span data-ttu-id="6b129-183">Указывает Длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="6b129-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-185">201</span><span class="sxs-lookup"><span data-stu-id="6b129-185">201</span></span></p></td>
<td><p><span data-ttu-id="6b129-186">Указывает значение длинной строкой.</span><span class="sxs-lookup"><span data-stu-id="6b129-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-188">203</span><span class="sxs-lookup"><span data-stu-id="6b129-188">203</span></span></p></td>
<td><p><span data-ttu-id="6b129-189">Указывает значение строки Юникод долго символом null.</span><span class="sxs-lookup"><span data-stu-id="6b129-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-191">131</span><span class="sxs-lookup"><span data-stu-id="6b129-191">131</span></span></p></td>
<td><p><span data-ttu-id="6b129-192">Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="6b129-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-194">138</span><span class="sxs-lookup"><span data-stu-id="6b129-194">138</span></span></p></td>
<td><p><span data-ttu-id="6b129-195">Указывает автоматизация PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="6b129-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-197">4</span><span class="sxs-lookup"><span data-stu-id="6b129-197">4</span></span></p></td>
<td><p><span data-ttu-id="6b129-198">Указывает значение с плавающей запятой одиночной точности (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="6b129-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-200">2</span><span class="sxs-lookup"><span data-stu-id="6b129-200">2</span></span></p></td>
<td><p><span data-ttu-id="6b129-201">Указывает двухбайтовые целого числа со знаком (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="6b129-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-203">16</span><span class="sxs-lookup"><span data-stu-id="6b129-203">16</span></span></p></td>
<td><p><span data-ttu-id="6b129-204">Указывает один байт целого числа со знаком (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="6b129-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-206">21</span><span class="sxs-lookup"><span data-stu-id="6b129-206">21</span></span></p></td>
<td><p><span data-ttu-id="6b129-207">Указывает, 8 байтовое целое (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="6b129-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-209">19</span><span class="sxs-lookup"><span data-stu-id="6b129-209">19</span></span></p></td>
<td><p><span data-ttu-id="6b129-210">Указывает, 4 байтовое целое число без знака (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="6b129-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-212">18</span><span class="sxs-lookup"><span data-stu-id="6b129-212">18</span></span></p></td>
<td><p><span data-ttu-id="6b129-213">Указывает, 2 байтовое целое число без знака (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="6b129-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-215">17</span><span class="sxs-lookup"><span data-stu-id="6b129-215">17</span></span></p></td>
<td><p><span data-ttu-id="6b129-216">Указывает один байтовое целое число без знака (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="6b129-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-218">132</span><span class="sxs-lookup"><span data-stu-id="6b129-218">132</span></span></p></td>
<td><p><span data-ttu-id="6b129-219">Указывает, определенные пользователем переменные (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="6b129-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-221">204</span><span class="sxs-lookup"><span data-stu-id="6b129-221">204</span></span></p></td>
<td><p><span data-ttu-id="6b129-222">Указывает двоичное значение (только для<strong>параметра</strong> объект).</span><span class="sxs-lookup"><span data-stu-id="6b129-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-224">200</span><span class="sxs-lookup"><span data-stu-id="6b129-224">200</span></span></p></td>
<td><p><span data-ttu-id="6b129-225">Указывает значение строки.</span><span class="sxs-lookup"><span data-stu-id="6b129-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-227">12</span><span class="sxs-lookup"><span data-stu-id="6b129-227">12</span></span></p></td>
<td><p><span data-ttu-id="6b129-228">Указывает, автоматизации <strong>Variant</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="6b129-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6b129-229">Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="6b129-229">This data type is currently not supported by ADO.</span></span> <span data-ttu-id="6b129-230">Применение может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="6b129-230">Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-232">139</span><span class="sxs-lookup"><span data-stu-id="6b129-232">139</span></span></p></td>
<td><p><span data-ttu-id="6b129-233">Указывает числовое значение (только для<strong>параметра</strong> объект).</span><span class="sxs-lookup"><span data-stu-id="6b129-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-235">202</span><span class="sxs-lookup"><span data-stu-id="6b129-235">202</span></span></p></td>
<td><p><span data-ttu-id="6b129-236">Указывает строку знаков Юникод символом null.</span><span class="sxs-lookup"><span data-stu-id="6b129-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-238">130</span><span class="sxs-lookup"><span data-stu-id="6b129-238">130</span></span></p></td>
<td><p><span data-ttu-id="6b129-239">Указывает строку знаков Юникод (DBTYPE_WSTR) символом null.</span><span class="sxs-lookup"><span data-stu-id="6b129-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6b129-240">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="6b129-240">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6b129-241">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6b129-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b129-242">Constant</span><span class="sxs-lookup"><span data-stu-id="6b129-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b129-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="6b129-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="6b129-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="6b129-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6b129-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="6b129-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="6b129-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="6b129-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="6b129-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="6b129-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="6b129-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="6b129-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="6b129-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="6b129-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="6b129-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="6b129-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="6b129-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="6b129-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="6b129-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="6b129-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="6b129-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="6b129-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="6b129-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6b129-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="6b129-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="6b129-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="6b129-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="6b129-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="6b129-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="6b129-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="6b129-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="6b129-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="6b129-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="6b129-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="6b129-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="6b129-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

