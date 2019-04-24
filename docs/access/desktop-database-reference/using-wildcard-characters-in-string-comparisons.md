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
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="ab2e3-102">Использование подстановочных знаков при сравнении строк</span><span class="sxs-lookup"><span data-stu-id="ab2e3-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="ab2e3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab2e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab2e3-104">Встроенная функция сопоставления шаблонов предоставляет многофункциональный инструмент для создания сравнений строк.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-104">Built-in pattern matching provides a versatile tool for making string comparisons.</span></span> <span data-ttu-id="ab2e3-105">В следующей таблице приведены подстановочные знаки, которые можно использовать с оператором **Like** , а также количество цифр и строк, которые они совпадают.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-105">The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab2e3-106">Символов в <em>шаблоне</em></span><span class="sxs-lookup"><span data-stu-id="ab2e3-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="ab2e3-107">Совпадений в <em>выражении</em></span><span class="sxs-lookup"><span data-stu-id="ab2e3-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab2e3-108">?</span><span class="sxs-lookup"><span data-stu-id="ab2e3-108"></span></span> <span data-ttu-id="ab2e3-109">или _ (подчеркивание)</span><span class="sxs-lookup"><span data-stu-id="ab2e3-109">or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="ab2e3-110">Любой знак</span><span class="sxs-lookup"><span data-stu-id="ab2e3-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2e3-111">\*также</span><span class="sxs-lookup"><span data-stu-id="ab2e3-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="ab2e3-112">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="ab2e3-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="ab2e3-113">Любая цифра (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="ab2e3-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2e3-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="ab2e3-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="ab2e3-115">Любой знак в группе <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="ab2e3-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p><span data-ttu-id="ab2e3-117">Любой знак вне группы <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="ab2e3-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab2e3-118">Вы можете использовать группу из одного или нескольких символов (*charlist*), заключенных в квадратные\[ \]скобки (), чтобы они содержали любой символ в *выражении,* а *charlist* может включать практически любой символ в набор ANSI-кодировки, в том числе знак.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="ab2e3-119">Вы можете использовать открывающую скобку символов (\[ ), вопросительный знак (_км_), решетку\#() и звездочку\*(), чтобы они непосредственно заключались в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="ab2e3-120">Нельзя использовать закрывающую квадратную скобку ( \]) в группе для самостоятельного согласования, но вы можете использовать ее за пределами группы в качестве отдельного знака.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="ab2e3-121">Помимо простого списка знаков, заключенных в скобки, группа *charlist* может задавать диапазон символов, используя дефис (-) для разделения верхней и нижней границ диапазона.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="ab2e3-122">Например, при использовании \[шаблона "A\] – \*\* z" результаты совпадают, если соответствующая позиция знака в *выражении* содержит любую из прописных букв в диапазоне от A до Z. Вы можете включить несколько диапазонов в квадратные скобки, не разделяя диапазоны.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="ab2e3-123">Например, \[a-zA-Z0-9\] соответствует любому буквенно-цифровому символу.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="ab2e3-124">Важно отметить, что подстановочные знаки ANSI SQL (%) и (\_) доступны только в Microsoft Jet версии 4. X и поставщику Microsoft OLE DB для Jet.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="ab2e3-125">Они будут рассматриваться как литералы, если они используются в Microsoft Access или DAO.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="ab2e3-126">Также имеются другие важные правила для сопоставления шаблона:</span><span class="sxs-lookup"><span data-stu-id="ab2e3-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="ab2e3-127">Восклицательный знак (\!) в начале *charlist* означает, что при обнаружении любого символа, кроме тех, которые находятся в *charlist* , в выражении \*\*.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="ab2e3-128">Если символ восклицательного знака используется без скобок, он сопоставляется с самим собой.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="ab2e3-129">Можно использовать дефис (-) в начале (после восклицательного знака, если он используется) или в конце *charlist* соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="ab2e3-130">В любом другом месте дефис определяет диапазон символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="ab2e3-131">Когда вы укажете диапазон символов, они должны отображаться в возрастающем порядке сортировки (A-Z или 0-100).</span><span class="sxs-lookup"><span data-stu-id="ab2e3-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="ab2e3-132">\[A – Z\] является допустимым шаблоном, \[А "Z\] -a" — нет.</span><span class="sxs-lookup"><span data-stu-id="ab2e3-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="ab2e3-133">Последовательность \[ \] символов игнорируется; считается строкой нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="ab2e3-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

