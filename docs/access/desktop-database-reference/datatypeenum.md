---
title: DataTypeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294444"
---
# <a name="datatypeenum"></a><span data-ttu-id="8bf4c-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="8bf4c-102">DataTypeEnum</span></span>

<span data-ttu-id="8bf4c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bf4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bf4c-104">Указывает тип данных [поля,](field-object-ado.md) [параметра](parameter-object-ado.md)или [свойства.](property-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8bf4c-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="8bf4c-105">Соответствующий индикатор типа OLE DB отображается в скобке в столбце описания следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="8bf4c-106">Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника по *OLE DB Programmer.*</span><span class="sxs-lookup"><span data-stu-id="8bf4c-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bf4c-107">Константа</span><span class="sxs-lookup"><span data-stu-id="8bf4c-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="8bf4c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf4c-108">Value</span></span></p></th>
<th><p><span data-ttu-id="8bf4c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8bf4c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="8bf4c-110"><strong>AdArray</span></span><br /><span data-ttu-id="8bf4c-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="8bf4c-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="8bf4c-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-113">Значение флага, всегда в сочетании с другой константой типа данных, которое указывает массив этого другого типа данных.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-115">20</span><span class="sxs-lookup"><span data-stu-id="8bf4c-115">20</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-116">Указывает на восьми bytete signed integer (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-118">128</span><span class="sxs-lookup"><span data-stu-id="8bf4c-118">128</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-119">Указывает двоичное значение (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-121">11</span><span class="sxs-lookup"><span data-stu-id="8bf4c-121">11</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-122">Указывает boolean value (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-124">8 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-124">8</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-125">Указывает строку символа с нулью (Юникод) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-127">136</span><span class="sxs-lookup"><span data-stu-id="8bf4c-127">136</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-128">Указывает четырех byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-130">129</span><span class="sxs-lookup"><span data-stu-id="8bf4c-130">129</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-131">Указывает строку (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-133">6 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-133">6</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-134">Указывает значение валюты (DBTYPE_CY).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="8bf4c-135">Валюта — это число с фиксированной точкой с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="8bf4c-136">Он хранится в 8-byte signed integer scaled by 10,000.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-138">7 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-138">7</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-139">Указывает значение даты (DBTYPE_DATE).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="8bf4c-140">Дата хранится в двойном номере, вся часть которого — это количество дней с 30 декабря 1899 г., а дробная часть — доля дня.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-142">133</span><span class="sxs-lookup"><span data-stu-id="8bf4c-142">133</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-143">Указывает значение даты (yyyymmdd) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-145">134</span><span class="sxs-lookup"><span data-stu-id="8bf4c-145">134</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-146">Указывает значение времени (ччммсс) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-148">135</span><span class="sxs-lookup"><span data-stu-id="8bf4c-148">135</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-149">Указывает отметку даты и времени (yyyymmddhhmmss плюс доля в DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-151">14 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-151">14</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-152">Указывает точное число с фиксированной точностью и масштабом (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-154">5 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-154">5</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-155">Указывает значение с плавающей за точкой двойной точности (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-157">0</span><span class="sxs-lookup"><span data-stu-id="8bf4c-157">0</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-158">Не указывает значение (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-160">10 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-160">10</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-161">Указывает 32-битный код ошибки (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-163">64</span><span class="sxs-lookup"><span data-stu-id="8bf4c-163">64</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-164">Указывает 64-битное значение, представляющее число интервалов в 100 наносекунд с 1 января 1601 г. (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-166">72</span><span class="sxs-lookup"><span data-stu-id="8bf4c-166">72</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-167">Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-169">9 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-169">9</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-170">Указывает указатель на <strong>интерфейс IDispatch</strong> объекта COM (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="8bf4c-171"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="8bf4c-172">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-174">3 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-174">3</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-175">Указывает на четырех bytete signed integer (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-177">13 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-177">13</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-178">Указывает указатель на интерфейс <strong>IUnknown</strong> в объекте COM (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="8bf4c-179"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="8bf4c-180">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-182">205</span><span class="sxs-lookup"><span data-stu-id="8bf4c-182">205</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-183">Указывает длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-185">201</span><span class="sxs-lookup"><span data-stu-id="8bf4c-185">201</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-186">Указывает длинное строку.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-188">203</span><span class="sxs-lookup"><span data-stu-id="8bf4c-188">203</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-189">Указывает длинное строкное значение Юникода, осекаемого нулью.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-191">131</span><span class="sxs-lookup"><span data-stu-id="8bf4c-191">131</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-192">Указывает точное число с фиксированной точностью и масштабом (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-194">138</span><span class="sxs-lookup"><span data-stu-id="8bf4c-194">138</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-195">Указывает automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-197">4 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-197">4</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-198">Указывает значение с плавающей за точкой с одной точностью (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-200">2 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-200">2</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-201">Указывает на двух bytete signed integer (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-203">16 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-203">16</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-204">Указывает одно bytete signed integer (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-206">21</span><span class="sxs-lookup"><span data-stu-id="8bf4c-206">21</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-207">Указывает восьми bytete unsigned integer (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-209">19</span><span class="sxs-lookup"><span data-stu-id="8bf4c-209">19</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-210">Указывает четырех bytete без подписи (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-212">18 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-212">18</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-213">Указывает двух bytete unsigned integer (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-215">17 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-215">17</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-216">Указывает одно byte-byte unsigned integer (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-218">132</span><span class="sxs-lookup"><span data-stu-id="8bf4c-218">132</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-219">Указывает определяемую пользователем переменную (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-221">204</span><span class="sxs-lookup"><span data-stu-id="8bf4c-221">204</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-222">Указывает двоичное значение (только<strong>объект Parameter).</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-224">200</span><span class="sxs-lookup"><span data-stu-id="8bf4c-224">200</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-225">Указывает строку.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-227">12 </span><span class="sxs-lookup"><span data-stu-id="8bf4c-227">12</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-228">Указывает вариант <strong>автоматизации</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="8bf4c-229"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="8bf4c-230">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-232">139</span><span class="sxs-lookup"><span data-stu-id="8bf4c-232">139</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-233">Указывает числовые значения ( только<strong>объект Parameter).</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-235">202</span><span class="sxs-lookup"><span data-stu-id="8bf4c-235">202</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-236">Указывает строку символа Юникода, осекаемую нулью.</span><span class="sxs-lookup"><span data-stu-id="8bf4c-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="8bf4c-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="8bf4c-238">130</span><span class="sxs-lookup"><span data-stu-id="8bf4c-238">130</span></span></p></td>
<td><p><span data-ttu-id="8bf4c-239">Указывает строку символа Юникода с нулью (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="8bf4c-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8bf4c-240">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8bf4c-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="8bf4c-241">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8bf4c-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bf4c-242">Константа</span><span class="sxs-lookup"><span data-stu-id="8bf4c-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8bf4c-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="8bf4c-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="8bf4c-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="8bf4c-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="8bf4c-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="8bf4c-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8bf4c-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="8bf4c-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="8bf4c-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="8bf4c-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="8bf4c-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="8bf4c-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="8bf4c-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="8bf4c-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="8bf4c-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="8bf4c-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="8bf4c-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="8bf4c-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="8bf4c-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bf4c-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bf4c-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="8bf4c-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

