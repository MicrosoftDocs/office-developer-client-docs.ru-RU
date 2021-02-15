---
title: Свойство Field.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ef68db39b7dcad380eae16f789f4dd5b0eab75f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292946"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="4a684-102">Свойство Field.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a684-102">Field.ValidationRule property (DAO)</span></span>


<span data-ttu-id="4a684-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a684-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a684-104">Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4a684-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="4a684-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="4a684-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a684-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a684-106">Syntax</span></span>

<span data-ttu-id="4a684-107">*выражение .* ValidationRule</span><span class="sxs-lookup"><span data-stu-id="4a684-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="4a684-108">*выражение* Выражение, которое возвращает объект **Field.**</span><span class="sxs-lookup"><span data-stu-id="4a684-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a684-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="4a684-109">Remarks</span></span>

<span data-ttu-id="4a684-110">Параметры или возвращаемые значения — это строка, описываемая сравнение в виде предложения SQL WHERE без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="4a684-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="4a684-111">Для объекта, еще не примежаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4a684-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="4a684-112">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="4a684-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="4a684-113">Если данные не являются допустимыми, возникает захватимая ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="4a684-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="4a684-114">Возвращенное сообщение об ошибке — это текст свойства **[ValidationText(если](field-validationtext-property-dao.md)** он указан) или текст выражения, указанного **в ValidationRule.**</span><span class="sxs-lookup"><span data-stu-id="4a684-114">The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="4a684-115">Для объекта **[Field](field-object-dao.md)** использование свойства **ValidationRule** зависит от объекта, который содержит коллекцию **Fields,** к которой применится объект **Field.**</span><span class="sxs-lookup"><span data-stu-id="4a684-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a684-116">Объект, к</span><span class="sxs-lookup"><span data-stu-id="4a684-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4a684-117">Использование</span><span class="sxs-lookup"><span data-stu-id="4a684-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a684-118"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="4a684-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4a684-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a684-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a684-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4a684-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4a684-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a684-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a684-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4a684-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4a684-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a684-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a684-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="4a684-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4a684-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a684-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a684-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4a684-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4a684-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4a684-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a684-128">Проверка поддерживается только для баз данных, которые используют ядер баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4a684-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="4a684-129">Строка выражения, заданного **свойством ValidationRule** объекта **Field,** может ссылаться только на это **поле.**</span><span class="sxs-lookup"><span data-stu-id="4a684-129">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="4a684-130">Выражение не может ссылаться на пользовательские функции, SQL агрегатные функции или запросы.</span><span class="sxs-lookup"><span data-stu-id="4a684-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="4a684-131">Чтобы установить свойство **ValidationRule** объекта **Field,** если его свойство **ValidateOnSet** имеет свойство **True,** выражение должно успешно синтаксировать (с именем поля в качестве подразумеваемого операнда) и оцениваться как **True**.</span><span class="sxs-lookup"><span data-stu-id="4a684-131">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="4a684-132">Если его **свойство ValidateOnSet** имеет свойство **False,** параметр **свойства ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4a684-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="4a684-133">Если для свойства задана строка, совмещенная с неиссякаемым значением, а системные параметры указывают не из США. десятичная символка, например запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), при попытке кода проверить любые данные будет выявить ошибку.</span><span class="sxs-lookup"><span data-stu-id="4a684-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="4a684-134">Это необходимо, так как во время конкатенации номер преобразуется в строку с помощью десятичных знаков системы по умолчанию, а подсистема баз данных Microsoft Access SQL принимает только десятичных знаков в США.</span><span class="sxs-lookup"><span data-stu-id="4a684-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


