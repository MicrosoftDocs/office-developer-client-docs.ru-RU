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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716903"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="0ee13-102">Использование подстановочных знаков при сравнении строк</span><span class="sxs-lookup"><span data-stu-id="0ee13-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="0ee13-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ee13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ee13-104">Встроенные подстановочные знаки представляет собой универсальный инструмент при осуществлении сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="0ee13-104">Built-in pattern matching provides a versatile tool for making string comparisons.</span></span> <span data-ttu-id="0ee13-105">В следующей таблице показаны подстановочные знаки, которые можно использовать с оператор **Like** и количество знаков или строк, которым они соответствуют.</span><span class="sxs-lookup"><span data-stu-id="0ee13-105">The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ee13-106">Символов в <em>шаблоне</em></span><span class="sxs-lookup"><span data-stu-id="0ee13-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="0ee13-107">Совпадений в <em>выражении</em></span><span class="sxs-lookup"><span data-stu-id="0ee13-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ee13-108">?</span><span class="sxs-lookup"><span data-stu-id="0ee13-108"></span></span> <span data-ttu-id="0ee13-109">или _ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="0ee13-109">or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="0ee13-110">Любой знак</span><span class="sxs-lookup"><span data-stu-id="0ee13-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ee13-111">\*или %</span><span class="sxs-lookup"><span data-stu-id="0ee13-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="0ee13-112">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="0ee13-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="0ee13-113">Любая отдельная цифра (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="0ee13-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ee13-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="0ee13-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="0ee13-115">Любой отдельный знак, представленный в <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="0ee13-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p><span data-ttu-id="0ee13-117">Любой отдельный знак, не представленный в <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="0ee13-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ee13-118">Можно использовать группы из одного или нескольких знаков (*charlist*) и заключенная в квадратные скобки (\[ \]) в соответствии с любой отдельный знак в *выражении* *charlist* можно добавить почти все символы символов ANSI задано, включая Количество цифр.</span><span class="sxs-lookup"><span data-stu-id="0ee13-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="0ee13-119">Можно использовать специальные символы Открытие скобка (\[ ), вопросительный знак (?), знак номера (\#) и звездочки (\*) для поиска других только если заключенная в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="0ee13-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="0ee13-120">Нельзя использовать закрывающая скобка ( \]) в группе в соответствии с самого, но его можно использовать вне группы как отдельный знак.</span><span class="sxs-lookup"><span data-stu-id="0ee13-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="0ee13-121">Помимо простого списка символов, заключенная в квадратные скобки *charlist* можно указать диапазон символов, используя дефис (-) для разделения верхние и нижние границы диапазона.</span><span class="sxs-lookup"><span data-stu-id="0ee13-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="0ee13-122">Например, с помощью \[A-Z\] в результатах *шаблон* в соответствие, если соответствующая позиция символа в *выражении* содержит какие-либо прописные буквы от A до Z. Можно включить несколько диапазонов в скобках, не запятая-разделитель диапазонов.</span><span class="sxs-lookup"><span data-stu-id="0ee13-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="0ee13-123">Например \[a-zA-Z0-9\] соответствует любой буквенно-цифровых символов.</span><span class="sxs-lookup"><span data-stu-id="0ee13-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="0ee13-124">Важно Обратите внимание, что подстановочные знаки (%) и (\_) можно только с помощью Microsoft Jet версии 4.X и поставщик Microsoft OLE DB для Jet.</span><span class="sxs-lookup"><span data-stu-id="0ee13-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="0ee13-125">Они будут рассматриваться как литералы, когда используются через Microsoft Access или DAO.</span><span class="sxs-lookup"><span data-stu-id="0ee13-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="0ee13-126">Также имеются другие важные правила для сопоставления шаблона:</span><span class="sxs-lookup"><span data-stu-id="0ee13-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="0ee13-127">Восклицательный знак (\!) в начале *charlist* означает, что соответствие устанавливается, если любой символ, за исключением тех, представленный в *charlist* находятся в *выражении*.</span><span class="sxs-lookup"><span data-stu-id="0ee13-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="0ee13-128">При использовании вне скобок восклицательный знак соответствует самой.</span><span class="sxs-lookup"><span data-stu-id="0ee13-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="0ee13-129">Можно использовать дефис (-) в начале (после восклицательный знак если таковой имеется) или в конце *charlist* для поиска.</span><span class="sxs-lookup"><span data-stu-id="0ee13-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="0ee13-130">В любом другом расположении дефис обозначает диапазон символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ee13-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="0ee13-131">При указании диапазон символов, символы должны быть указаны в порядке возрастания (A-Z или 0-100).</span><span class="sxs-lookup"><span data-stu-id="0ee13-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="0ee13-132">\[A-Z\] является допустимым шаблоном, но \[Z-A\] не является.</span><span class="sxs-lookup"><span data-stu-id="0ee13-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="0ee13-133">Последовательность знаков \[ \] , игнорируются. он считается строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="0ee13-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

