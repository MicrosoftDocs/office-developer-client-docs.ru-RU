---
title: DataTypeEnum (Справочник по базам данных Access на компьютере)
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
# <a name="datatypeenum"></a><span data-ttu-id="2aa2a-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="2aa2a-102">DataTypeEnum</span></span>

<span data-ttu-id="2aa2a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2aa2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2aa2a-104">Указывает тип данных [поля](field-object-ado.md), [параметра](parameter-object-ado.md)или [Свойства](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="2aa2a-105">Соответствующий индикатор типа OLE DB отображается в круглых скобках в столбце Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="2aa2a-106">Дополнительные сведения о типах данных OLE DB приведены в главе 13 и приложении A *Справочника программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2aa2a-107">Константа</span><span class="sxs-lookup"><span data-stu-id="2aa2a-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="2aa2a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2aa2a-108">Value</span></span></p></th>
<th><p><span data-ttu-id="2aa2a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa2a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-110"><strong>адаррай</span><span class="sxs-lookup"><span data-stu-id="2aa2a-110"><strong>AdArray</span></span><br /><span data-ttu-id="2aa2a-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="2aa2a-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="2aa2a-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-113">Значение флага, всегда скомбинированное с другой константой типа данных, которое указывает массив другого типа данных.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-114"><strong>адбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-115">двадцать</span><span class="sxs-lookup"><span data-stu-id="2aa2a-115">20</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-116">Указывает 8-разрядное целое число со знаком (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-117"><strong>адбинари</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-118">128</span><span class="sxs-lookup"><span data-stu-id="2aa2a-118">128</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-119">Указывает двоичное значение (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-120"><strong>адбулеан</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-121">11 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-121">11</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-122">Указывает логическое значение (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-123"><strong>адбстр</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-124">8 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-124">8</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-125">Указывает строку символов (Юникод), заканчивающуюся нулем (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-126"><strong>адчаптер</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-127">136</span><span class="sxs-lookup"><span data-stu-id="2aa2a-127">136</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-128">Указывает значение главы из четырех байт, которое определяет строки в дочернем наборе строк (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-129"><strong>адчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-130">129</span><span class="sxs-lookup"><span data-stu-id="2aa2a-130">129</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-131">Указывает строковое значение (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-132"><strong>адкурренци</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-133">6 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-133">6</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-134">Показывает значение валюты (DBTYPE_CY).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="2aa2a-135">Currency — это число с фиксированной запятой, сопоставленное с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="2aa2a-136">Он хранится в виде целого числа со знаком длиной 8 байт, масштабированное на 10 000.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-137"><strong>аддате</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-138">7 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-138">7</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-139">Указывает значение даты (DBTYPE_DATE).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="2aa2a-140">Дата хранится в виде Double, целой части, которая представляет собой количество дней с 30 декабря 1899 г., и дробная часть, представляющая долю дня.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-141"><strong>аддбдате</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-142">133</span><span class="sxs-lookup"><span data-stu-id="2aa2a-142">133</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-143">Указывает значение даты (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-144"><strong>аддбтиме</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-145">134</span><span class="sxs-lookup"><span data-stu-id="2aa2a-145">134</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-146">Указывает значение времени (ЧЧММСС) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-147"><strong>аддбтиместамп</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-148">135</span><span class="sxs-lookup"><span data-stu-id="2aa2a-148">135</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-149">Указывает отметку даты и времени (ГГГГММДДЧЧММСС плюс дробь в биллионсс) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-150"><strong>аддеЦимал</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-151">14 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-151">14</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-152">Указывает точное числовое значение с фиксированной точностью и масштабом (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-153"><strong>аддаубле</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-154">5 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-154">5</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-155">Указывает значение двойной точности с плавающей запятой (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-156"><strong>адемпти</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-157">нуль</span><span class="sxs-lookup"><span data-stu-id="2aa2a-157">0</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-158">Значение не задано (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-159"><strong>адеррор</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-160">10 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-160">10</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-161">Указывает 32-разрядный код ошибки (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-162"><strong>адфилетиме</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-163">64</span><span class="sxs-lookup"><span data-stu-id="2aa2a-163">64</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-164">Указывает 64-разрядное значение, представляющее количество интервалов 100-наносекундных с 1 января 1601 г. (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-165"><strong>адгуид</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-166">72</span><span class="sxs-lookup"><span data-stu-id="2aa2a-166">72</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-167">Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-168"><strong>адидиспатч</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-169">9 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-169">9</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-170">Показывает указатель на интерфейс <strong>IDispatch</strong> объекта COM (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="2aa2a-171"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="2aa2a-172">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-173"><strong>адинтежер</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-174">4</span><span class="sxs-lookup"><span data-stu-id="2aa2a-174">3</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-175">Указывает 4-разрядное целое число со знаком (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-176"><strong>адиункновн</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-177">13</span><span class="sxs-lookup"><span data-stu-id="2aa2a-177">13</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-178">Показывает указатель на интерфейс <strong>IUnknown</strong> для объекта COM (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="2aa2a-179"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="2aa2a-180">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-181"><strong>адлонгварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-182">205</span><span class="sxs-lookup"><span data-stu-id="2aa2a-182">205</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-183">Указывает длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-184"><strong>адлонгварчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-185">201</span><span class="sxs-lookup"><span data-stu-id="2aa2a-185">201</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-186">Указывает длинное строковое значение.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-187"><strong>адлонгварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-188">203</span><span class="sxs-lookup"><span data-stu-id="2aa2a-188">203</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-189">Указывает длинное строковое значение Юникода с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-190"><strong>аднумерик</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-191">131</span><span class="sxs-lookup"><span data-stu-id="2aa2a-191">131</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-192">Указывает точное числовое значение с фиксированной точностью и масштабом (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-193"><strong>адпропвариант</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-194">138</span><span class="sxs-lookup"><span data-stu-id="2aa2a-194">138</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-195">Указывает ПРОПВАРИАНТ автоматизации (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-196"><strong>адсингле</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-197">4 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-197">4</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-198">Показывает значение одиночной точности с плавающей запятой (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-199"><strong>адсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-200">2</span><span class="sxs-lookup"><span data-stu-id="2aa2a-200">2</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-201">Указывает 2-байтовое целое число со знаком (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-202"><strong>адтининт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-203">16 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-203">16</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-204">Указывает Однобайтовое целое со знаком (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-205"><strong>адунсигнедбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-206">21</span><span class="sxs-lookup"><span data-stu-id="2aa2a-206">21</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-207">Указывает целое число без знака длиной 8 байт (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-208"><strong>адунсигнединт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-209">19</span><span class="sxs-lookup"><span data-stu-id="2aa2a-209">19</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-210">Указывает целое число без знака длиной 4 байта (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-211"><strong>адунсигнедсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-212">18 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-212">18</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-213">Указывает на неподписанное 2-разрядное целое число (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-214"><strong>адунсигнедтининт</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-215">17 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-215">17</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-216">Указывает Однобайтовое целое число без знака (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-217"><strong>адусердефинед</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-218">132</span><span class="sxs-lookup"><span data-stu-id="2aa2a-218">132</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-219">Указывает пользовательскую переменную (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-220"><strong>адварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-221">204</span><span class="sxs-lookup"><span data-stu-id="2aa2a-221">204</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-222">Указывает двоичное значение (только для объекта<strong>Parameter</strong> ).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-223"><strong>адварчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-224">200</span><span class="sxs-lookup"><span data-stu-id="2aa2a-224">200</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-225">Указывает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-226"><strong>адвариант</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-227">12 </span><span class="sxs-lookup"><span data-stu-id="2aa2a-227">12</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-228">Указывает на <strong>вариант</strong> автоматизации (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="2aa2a-229"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="2aa2a-230">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-231"><strong>адварнумерик</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-232">139</span><span class="sxs-lookup"><span data-stu-id="2aa2a-232">139</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-233">Указывает числовое значение (только для объекта<strong>Parameter</strong> ).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-234"><strong>адварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-235">202</span><span class="sxs-lookup"><span data-stu-id="2aa2a-235">202</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-236">Указывает строку символов Юникода, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="2aa2a-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-237"><strong>адвчар</strong></span><span class="sxs-lookup"><span data-stu-id="2aa2a-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2aa2a-238">130</span><span class="sxs-lookup"><span data-stu-id="2aa2a-238">130</span></span></p></td>
<td><p><span data-ttu-id="2aa2a-239">Указывает строку символов Юникода, заканчивающуюся нулем (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="2aa2a-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2aa2a-240">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2aa2a-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="2aa2a-241">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="2aa2a-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2aa2a-242">Константа</span><span class="sxs-lookup"><span data-stu-id="2aa2a-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-243">Адоенумс. DataType. ARRAY</span><span class="sxs-lookup"><span data-stu-id="2aa2a-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-244">Адоенумс. DataType. BIGINT</span><span class="sxs-lookup"><span data-stu-id="2aa2a-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-245">Адоенумс. DataType. BINARY</span><span class="sxs-lookup"><span data-stu-id="2aa2a-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-246">Адоенумс. DataType. BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2aa2a-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-247">Адоенумс. DataType. BSTR</span><span class="sxs-lookup"><span data-stu-id="2aa2a-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-248">Адоенумс. DataType. CHAPTER</span><span class="sxs-lookup"><span data-stu-id="2aa2a-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-249">Адоенумс. DataType. CHAR</span><span class="sxs-lookup"><span data-stu-id="2aa2a-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-250">Адоенумс. DataType. CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2aa2a-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-251">Адоенумс. DataType. DATE</span><span class="sxs-lookup"><span data-stu-id="2aa2a-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-252">Адоенумс. DataType. ДБДАТЕ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-253">Адоенумс. DataType. ДБТИМЕ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-254">Адоенумс. DataType. ДБТИМЕСТАМП</span><span class="sxs-lookup"><span data-stu-id="2aa2a-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-255">Адоенумс. DataType. DECIMAL</span><span class="sxs-lookup"><span data-stu-id="2aa2a-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-256">Адоенумс. DataType. DOUBLE</span><span class="sxs-lookup"><span data-stu-id="2aa2a-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-257">Адоенумс. DataType. EMPTY</span><span class="sxs-lookup"><span data-stu-id="2aa2a-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-258">Адоенумс. DataType. ERROR</span><span class="sxs-lookup"><span data-stu-id="2aa2a-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-259">Адоенумс. DataType. FILETIME</span><span class="sxs-lookup"><span data-stu-id="2aa2a-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-260">Адоенумс. DataType. GUID</span><span class="sxs-lookup"><span data-stu-id="2aa2a-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-261">Адоенумс. DataType. IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="2aa2a-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-262">Адоенумс. DataType. INTEGER</span><span class="sxs-lookup"><span data-stu-id="2aa2a-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-263">Адоенумс. DataType. IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="2aa2a-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-264">Адоенумс. DataType. ЛОНГВАРБИНАРИ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-265">Адоенумс. DataType. ЛОНГВАРЧАР</span><span class="sxs-lookup"><span data-stu-id="2aa2a-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-266">Адоенумс. DataType. ЛОНГВАРВЧАР</span><span class="sxs-lookup"><span data-stu-id="2aa2a-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-267">Адоенумс. DataType. NUMERIC</span><span class="sxs-lookup"><span data-stu-id="2aa2a-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-268">Адоенумс. DataType. ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-269">Адоенумс. DataType. SINGLE</span><span class="sxs-lookup"><span data-stu-id="2aa2a-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-270">Адоенумс. DataType. SMALLINT</span><span class="sxs-lookup"><span data-stu-id="2aa2a-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-271">Адоенумс. DataType. TINYINT</span><span class="sxs-lookup"><span data-stu-id="2aa2a-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-272">Адоенумс. DataType. УНСИГНЕДБИГИНТ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-273">Адоенумс. DataType. УНСИГНЕДИНТ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-274">Адоенумс. DataType. УНСИГНЕДСМАЛЛИНТ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-275">Адоенумс. DataType. УНСИГНЕДТИНИНТ</span><span class="sxs-lookup"><span data-stu-id="2aa2a-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-276">Адоенумс. DataType. USERDEFINED типа</span><span class="sxs-lookup"><span data-stu-id="2aa2a-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-277">Адоенумс. DataType. VARBINARY</span><span class="sxs-lookup"><span data-stu-id="2aa2a-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-278">Адоенумс. DataType. VARCHAR</span><span class="sxs-lookup"><span data-stu-id="2aa2a-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-279">Адоенумс. DataType. VARIANT</span><span class="sxs-lookup"><span data-stu-id="2aa2a-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-280">Адоенумс. DataType. ВАРНУМЕРИК</span><span class="sxs-lookup"><span data-stu-id="2aa2a-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aa2a-281">Адоенумс. DataType. ВАРВЧАР</span><span class="sxs-lookup"><span data-stu-id="2aa2a-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aa2a-282">Адоенумс. DataType. WCHAR</span><span class="sxs-lookup"><span data-stu-id="2aa2a-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

