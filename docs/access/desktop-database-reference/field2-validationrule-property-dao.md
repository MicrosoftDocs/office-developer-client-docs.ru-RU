---
title: Свойство Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292652"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="0eb91-102">Свойство Field2.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="0eb91-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="0eb91-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0eb91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0eb91-104">Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0eb91-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0eb91-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="0eb91-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb91-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eb91-106">Syntax</span></span>

<span data-ttu-id="0eb91-107">*выражение .* ValidationRule</span><span class="sxs-lookup"><span data-stu-id="0eb91-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="0eb91-108">*выражение* Выражение, которое возвращает **объект Field2.**</span><span class="sxs-lookup"><span data-stu-id="0eb91-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb91-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="0eb91-109">Remarks</span></span>

<span data-ttu-id="0eb91-110">Параметры или возвращаемые значения — это строка, описываемая сравнение в виде предложения SQL WHERE без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="0eb91-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="0eb91-111">Для объекта, еще не примежаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0eb91-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="0eb91-112">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="0eb91-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="0eb91-113">Если данные не являются допустимыми, возникает захватимая ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="0eb91-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="0eb91-114">Возвращенное сообщение об ошибке — это текст свойства **ValidationText(если** он указан) или текст выражения, указанного **в ValidationRule.**</span><span class="sxs-lookup"><span data-stu-id="0eb91-114">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="0eb91-115">Для объекта **Field2** использование свойства **ValidationRule** зависит от объекта, который содержит коллекцию **Fields,** к которой применится объект **Field2.**</span><span class="sxs-lookup"><span data-stu-id="0eb91-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0eb91-116">Объект, к</span><span class="sxs-lookup"><span data-stu-id="0eb91-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="0eb91-117">Использование</span><span class="sxs-lookup"><span data-stu-id="0eb91-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0eb91-118"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="0eb91-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="0eb91-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0eb91-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0eb91-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0eb91-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0eb91-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb91-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0eb91-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0eb91-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="0eb91-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb91-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0eb91-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0eb91-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="0eb91-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0eb91-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0eb91-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0eb91-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0eb91-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0eb91-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0eb91-128">Проверка поддерживается только для баз данных, в которые используется ядер баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0eb91-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="0eb91-129">Строка выражения, заданного **свойством ValidationRule** объекта **Field2,** может относиться только **к этому Field2**.</span><span class="sxs-lookup"><span data-stu-id="0eb91-129">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**.</span></span> <span data-ttu-id="0eb91-130">Выражение не может ссылаться на пользовательские функции, SQL агрегатные функции или запросы.</span><span class="sxs-lookup"><span data-stu-id="0eb91-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="0eb91-131">Чтобы установить свойство **ValidationRule** объекта **Field2,** если его свойство **ValidateOnSet** имеет свойство **True,** выражение должно успешно синтаксировать (с именем поля в качестве подразумеваемого операнда) и оцениваться как **True**.</span><span class="sxs-lookup"><span data-stu-id="0eb91-131">To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="0eb91-132">Если его **свойство ValidateOnSet** имеет свойство **False,** параметр **свойства ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0eb91-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="0eb91-133">Если для свойства задана строка, совмещенная с неиссякаемым значением, а системные параметры указывают не из США. десятичная символка, например запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), при попытке кода проверить любые данные будет выявить ошибку.</span><span class="sxs-lookup"><span data-stu-id="0eb91-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="0eb91-134">Это необходимо, так как во время конкатенации номер преобразуется в строку с помощью десятичных знаков по умолчанию вашей системы, а подсистема баз данных Microsoft Access SQL принимает только десятичных знаков в США.</span><span class="sxs-lookup"><span data-stu-id="0eb91-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


