---
title: Использование подстановочных знаков при сравнении строк
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305938"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="3c03e-102">Использование подстановочных знаков при сравнении строк</span><span class="sxs-lookup"><span data-stu-id="3c03e-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="3c03e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c03e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c03e-104">Встроенная функция сопоставления шаблонов предоставляет многофункциональный инструмент для создания сравнений строк.</span><span class="sxs-lookup"><span data-stu-id="3c03e-104">Built-in pattern matching provides a versatile tool for making string comparisons.</span></span> <span data-ttu-id="3c03e-105">В следующей таблице показаны поддеревные знаки, которые можно использовать с оператором **Like,** а также количество цифр или строк, которые они соответствуют.</span><span class="sxs-lookup"><span data-stu-id="3c03e-105">The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c03e-106">Символов в <em>шаблоне</em></span><span class="sxs-lookup"><span data-stu-id="3c03e-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="3c03e-107">Совпадений в <em>выражении</em></span><span class="sxs-lookup"><span data-stu-id="3c03e-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c03e-108">?</span><span class="sxs-lookup"><span data-stu-id="3c03e-108">?</span></span> <span data-ttu-id="3c03e-109">или _ (подчеркивать)</span><span class="sxs-lookup"><span data-stu-id="3c03e-109">or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="3c03e-110">Любой знак</span><span class="sxs-lookup"><span data-stu-id="3c03e-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c03e-111">\* или %</span><span class="sxs-lookup"><span data-stu-id="3c03e-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="3c03e-112">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="3c03e-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="3c03e-113">Любая одна цифра (0–9)</span><span class="sxs-lookup"><span data-stu-id="3c03e-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c03e-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="3c03e-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="3c03e-115">Любой знак в группе <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="3c03e-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c03e-116">[! <em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="3c03e-116">[!<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="3c03e-117">Любой знак вне группы <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="3c03e-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c03e-118">Вы можете использовать группу из одного или более символов *(charlist),* заключенных в скобки ( ) для совпадения любого отдельного символа в выражении, а список символов может включать почти любые символы в наборе символов \[ \] ANSI, включая цифры.  </span><span class="sxs-lookup"><span data-stu-id="3c03e-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="3c03e-119">Специальные символы, открывая скобки ( ), вопросии (?), знак номера ( ) и звездочка ( ), можно использовать для непосредственного совпадения, только если заключены в \[ \# \* скобки.</span><span class="sxs-lookup"><span data-stu-id="3c03e-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="3c03e-120">Вы не можете использовать закрываюю скобку () внутри группы, чтобы соответствовать самой себе, но вы можете использовать ее за пределами группы в \] качестве отдельного символа.</span><span class="sxs-lookup"><span data-stu-id="3c03e-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="3c03e-121">Помимо простого списка знаков, заключенных в скобки, группа *charlist* может задавать диапазон символов, используя дефис (-) для разделения верхней и нижней границ диапазона.</span><span class="sxs-lookup"><span data-stu-id="3c03e-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="3c03e-122">Например, использование шаблона A-Z приводит к совпадению, если соответствующее положение символа в выражении содержит любую из верхних букв в диапазоне \[ \] от A до Z.   Можно включить несколько диапазонов в квадратные скобки без деления диапазонов.</span><span class="sxs-lookup"><span data-stu-id="3c03e-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="3c03e-123">Например, \[ a-zA-Z0-9 \] соответствует любому букво-цифровую символу.</span><span class="sxs-lookup"><span data-stu-id="3c03e-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="3c03e-124">Важно отметить, что SQL anSI (%) и ( \_ ) доступны только в Microsoft Jet версии 4.X и поставщике Microsoft OLE DB для Jet.</span><span class="sxs-lookup"><span data-stu-id="3c03e-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="3c03e-125">Они будут рассматриваться как литералы, если они используются через Microsoft Access или DAO.</span><span class="sxs-lookup"><span data-stu-id="3c03e-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="3c03e-126">Также имеются другие важные правила для сопоставления шаблона:</span><span class="sxs-lookup"><span data-stu-id="3c03e-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="3c03e-127">Восклицательный знак ( ) в начале charlist означает, что совпадение будет выполнено, если в выражении найдены какие-либо символы, кроме тех, которые находятся \! в *списке*  символов. </span><span class="sxs-lookup"><span data-stu-id="3c03e-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="3c03e-128">Если символ восклицательного знака используется без скобок, он сопоставляется с самим собой.</span><span class="sxs-lookup"><span data-stu-id="3c03e-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="3c03e-129">Вы можете использовать дефис (-) в начале (после восклицательный знак, если он используется) или в конце *списка charlist,* чтобы соответствовать самому себе.</span><span class="sxs-lookup"><span data-stu-id="3c03e-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="3c03e-130">В любом другом расположении дефис определяет диапазон символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="3c03e-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="3c03e-131">При указании диапазона символов символы должны отображаться в порядке возрастания (A-Z или 0–100).</span><span class="sxs-lookup"><span data-stu-id="3c03e-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="3c03e-132">\[A-Z \] — допустимый шаблон, а \[ Z-A \] — нет.</span><span class="sxs-lookup"><span data-stu-id="3c03e-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="3c03e-133">Последовательность символов игнорируется; она считается строкой \[ \] нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="3c03e-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

