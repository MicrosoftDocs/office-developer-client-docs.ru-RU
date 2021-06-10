---
title: DataTypeEnum (Ссылка на настольные базы данных)
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
# <a name="datatypeenum"></a><span data-ttu-id="44145-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="44145-102">DataTypeEnum</span></span>

<span data-ttu-id="44145-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44145-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44145-104">Указывает тип данных [поля,](field-object-ado.md) [параметра](parameter-object-ado.md)или [свойства.](property-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="44145-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="44145-105">Соответствующий индикатор типа OLE DB показан в скобки в столбце описания следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="44145-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="44145-106">Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника программиста *OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="44145-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44145-107">Константа</span><span class="sxs-lookup"><span data-stu-id="44145-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="44145-108">Значение</span><span class="sxs-lookup"><span data-stu-id="44145-108">Value</span></span></p></th>
<th><p><span data-ttu-id="44145-109">Описание</span><span class="sxs-lookup"><span data-stu-id="44145-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44145-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="44145-110"><strong>AdArray</span></span><br /><span data-ttu-id="44145-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="44145-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="44145-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="44145-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="44145-113">Значение флага, всегда в сочетании с константой другого типа данных, указывает массив этого другого типа данных.</span><span class="sxs-lookup"><span data-stu-id="44145-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-115">20</span><span class="sxs-lookup"><span data-stu-id="44145-115">20</span></span></p></td>
<td><p><span data-ttu-id="44145-116">Указывает на подписанный в восемь byte integer (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="44145-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44145-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-118">128</span><span class="sxs-lookup"><span data-stu-id="44145-118">128</span></span></p></td>
<td><p><span data-ttu-id="44145-119">Указывает двоичное значение (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="44145-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="44145-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-121">11</span><span class="sxs-lookup"><span data-stu-id="44145-121">11</span></span></p></td>
<td><p><span data-ttu-id="44145-122">Указывает значение boolean (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="44145-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="44145-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-124">8 </span><span class="sxs-lookup"><span data-stu-id="44145-124">8</span></span></p></td>
<td><p><span data-ttu-id="44145-125">Указывает null-terminated character string (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="44145-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="44145-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-127">136</span><span class="sxs-lookup"><span data-stu-id="44145-127">136</span></span></p></td>
<td><p><span data-ttu-id="44145-128">Указывает значение главы с четырьмя byte, которое определяет строки в детском наборе строк (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="44145-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-130">129</span><span class="sxs-lookup"><span data-stu-id="44145-130">129</span></span></p></td>
<td><p><span data-ttu-id="44145-131">Указывает значение строки (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="44145-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="44145-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-133">6 </span><span class="sxs-lookup"><span data-stu-id="44145-133">6</span></span></p></td>
<td><p><span data-ttu-id="44145-134">Указывает значение валюты (DBTYPE_CY).</span><span class="sxs-lookup"><span data-stu-id="44145-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="44145-135">Валюта — это номер фиксированной точки с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="44145-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="44145-136">Он хранится в подписанном на восемь byte integer масштабе 10 000.</span><span class="sxs-lookup"><span data-stu-id="44145-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="44145-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-138">7 </span><span class="sxs-lookup"><span data-stu-id="44145-138">7</span></span></p></td>
<td><p><span data-ttu-id="44145-139">Указывает значение даты (DBTYPE_DATE).</span><span class="sxs-lookup"><span data-stu-id="44145-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="44145-140">Дата хранится как двойная, вся часть которой — это количество дней с 30 декабря 1899 г., а фракционной частью которой является доля дня.</span><span class="sxs-lookup"><span data-stu-id="44145-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="44145-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-142">133</span><span class="sxs-lookup"><span data-stu-id="44145-142">133</span></span></p></td>
<td><p><span data-ttu-id="44145-143">Указывает значение даты (yyyyymmdd) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="44145-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="44145-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-145">134</span><span class="sxs-lookup"><span data-stu-id="44145-145">134</span></span></p></td>
<td><p><span data-ttu-id="44145-146">Указывает значение времени (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="44145-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="44145-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-148">135</span><span class="sxs-lookup"><span data-stu-id="44145-148">135</span></span></p></td>
<td><p><span data-ttu-id="44145-149">Указывает штамп даты и времени (yyyymmddhhmmss плюс доля в миллиардных долях) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="44145-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="44145-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-151">14 </span><span class="sxs-lookup"><span data-stu-id="44145-151">14</span></span></p></td>
<td><p><span data-ttu-id="44145-152">Указывает точное численное значение с фиксированной точностью и масштабом (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="44145-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="44145-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-154">5 </span><span class="sxs-lookup"><span data-stu-id="44145-154">5</span></span></p></td>
<td><p><span data-ttu-id="44145-155">Указывает значение плавающей точки с двойной точностью (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="44145-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="44145-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-157">0</span><span class="sxs-lookup"><span data-stu-id="44145-157">0</span></span></p></td>
<td><p><span data-ttu-id="44145-158">Не указывает значения (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="44145-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="44145-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-160">10 </span><span class="sxs-lookup"><span data-stu-id="44145-160">10</span></span></p></td>
<td><p><span data-ttu-id="44145-161">Указывает 32-битный код ошибки (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="44145-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="44145-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-163">64</span><span class="sxs-lookup"><span data-stu-id="44145-163">64</span></span></p></td>
<td><p><span data-ttu-id="44145-164">Указывает 64-битное значение, представляющее число 100-наносекундных интервалов с 1 января 1601 г. (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="44145-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="44145-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-166">72</span><span class="sxs-lookup"><span data-stu-id="44145-166">72</span></span></p></td>
<td><p><span data-ttu-id="44145-167">Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="44145-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="44145-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-169">9 </span><span class="sxs-lookup"><span data-stu-id="44145-169">9</span></span></p></td>
<td><p><span data-ttu-id="44145-170">Указывает указатель на интерфейс <strong>IDispatch</strong> на объекте COM (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="44145-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="44145-171"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="44145-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="44145-172">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="44145-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="44145-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-174">3</span><span class="sxs-lookup"><span data-stu-id="44145-174">3</span></span></p></td>
<td><p><span data-ttu-id="44145-175">Указывает на подписанный в четырех byte ряд (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="44145-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="44145-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-177">13</span><span class="sxs-lookup"><span data-stu-id="44145-177">13</span></span></p></td>
<td><p><span data-ttu-id="44145-178">Указывает указатель на <strong>интерфейс IUnknown</strong> на объекте COM (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="44145-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="44145-179"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="44145-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="44145-180">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="44145-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44145-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-182">205</span><span class="sxs-lookup"><span data-stu-id="44145-182">205</span></span></p></td>
<td><p><span data-ttu-id="44145-183">Указывает длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="44145-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-185">201</span><span class="sxs-lookup"><span data-stu-id="44145-185">201</span></span></p></td>
<td><p><span data-ttu-id="44145-186">Указывает значение длинной строки.</span><span class="sxs-lookup"><span data-stu-id="44145-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-188">203</span><span class="sxs-lookup"><span data-stu-id="44145-188">203</span></span></p></td>
<td><p><span data-ttu-id="44145-189">Указывает значение строки Юникод с длинным null-terminated.</span><span class="sxs-lookup"><span data-stu-id="44145-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="44145-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-191">131</span><span class="sxs-lookup"><span data-stu-id="44145-191">131</span></span></p></td>
<td><p><span data-ttu-id="44145-192">Указывает точное численное значение с фиксированной точностью и масштабом (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="44145-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="44145-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-194">138</span><span class="sxs-lookup"><span data-stu-id="44145-194">138</span></span></p></td>
<td><p><span data-ttu-id="44145-195">Указывает средства автоматизации PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="44145-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="44145-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-197">4 </span><span class="sxs-lookup"><span data-stu-id="44145-197">4</span></span></p></td>
<td><p><span data-ttu-id="44145-198">Указывает одноточное значение плавающей точки (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="44145-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-200">2</span><span class="sxs-lookup"><span data-stu-id="44145-200">2</span></span></p></td>
<td><p><span data-ttu-id="44145-201">Указывает на двухбетный подписанный ряд (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="44145-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-203">16 </span><span class="sxs-lookup"><span data-stu-id="44145-203">16</span></span></p></td>
<td><p><span data-ttu-id="44145-204">Указывает на одноайтовую подпись (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="44145-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-206">21</span><span class="sxs-lookup"><span data-stu-id="44145-206">21</span></span></p></td>
<td><p><span data-ttu-id="44145-207">Указывает неподписаный неподписаный 8-кет (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="44145-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-209">19</span><span class="sxs-lookup"><span data-stu-id="44145-209">19</span></span></p></td>
<td><p><span data-ttu-id="44145-210">Указывает неподписаный четверной ряд (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="44145-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-212">18 </span><span class="sxs-lookup"><span data-stu-id="44145-212">18</span></span></p></td>
<td><p><span data-ttu-id="44145-213">Указывает на неподписавую неподписаемую DBTYPE_UI2.</span><span class="sxs-lookup"><span data-stu-id="44145-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="44145-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-215">17 </span><span class="sxs-lookup"><span data-stu-id="44145-215">17</span></span></p></td>
<td><p><span data-ttu-id="44145-216">Указывает на неподписавую неподписаемую неподписаемую DBTYPE_UI1.</span><span class="sxs-lookup"><span data-stu-id="44145-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="44145-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-218">132</span><span class="sxs-lookup"><span data-stu-id="44145-218">132</span></span></p></td>
<td><p><span data-ttu-id="44145-219">Указывает переменную, определяемую пользователем (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="44145-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44145-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-221">204</span><span class="sxs-lookup"><span data-stu-id="44145-221">204</span></span></p></td>
<td><p><span data-ttu-id="44145-222">Указывает двоичное значение<strong>(только объект Параметр).</strong></span><span class="sxs-lookup"><span data-stu-id="44145-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-224">200</span><span class="sxs-lookup"><span data-stu-id="44145-224">200</span></span></p></td>
<td><p><span data-ttu-id="44145-225">Указывает строковую величину.</span><span class="sxs-lookup"><span data-stu-id="44145-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="44145-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-227">12 </span><span class="sxs-lookup"><span data-stu-id="44145-227">12</span></span></p></td>
<td><p><span data-ttu-id="44145-228">Указывает вариант <strong>автоматизации</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="44145-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="44145-229"><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="44145-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="44145-230">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="44145-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="44145-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-232">139</span><span class="sxs-lookup"><span data-stu-id="44145-232">139</span></span></p></td>
<td><p><span data-ttu-id="44145-233">Указывает численное значение<strong>(только объект Параметр).</strong></span><span class="sxs-lookup"><span data-stu-id="44145-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-235">202</span><span class="sxs-lookup"><span data-stu-id="44145-235">202</span></span></p></td>
<td><p><span data-ttu-id="44145-236">Указывает строку символов Юникод с null-terminated.</span><span class="sxs-lookup"><span data-stu-id="44145-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44145-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44145-238">130</span><span class="sxs-lookup"><span data-stu-id="44145-238">130</span></span></p></td>
<td><p><span data-ttu-id="44145-239">Указывает строку символов Юникод с null-terminated (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="44145-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="44145-240">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="44145-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="44145-241">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="44145-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44145-242">Константа</span><span class="sxs-lookup"><span data-stu-id="44145-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44145-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="44145-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="44145-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="44145-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="44145-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="44145-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="44145-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="44145-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="44145-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="44145-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="44145-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="44145-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="44145-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="44145-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="44145-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="44145-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="44145-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="44145-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="44145-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="44145-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="44145-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="44145-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="44145-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="44145-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="44145-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="44145-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="44145-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="44145-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="44145-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="44145-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="44145-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="44145-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="44145-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="44145-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="44145-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="44145-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="44145-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="44145-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="44145-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44145-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="44145-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44145-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="44145-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

