---
title: Field.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a737f19b33777ea9c3acaf3bc6a9de5144a4db6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874078"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="1a62e-102">Field.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a62e-102">Field.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="1a62e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a62e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a62e-104">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1a62e-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="1a62e-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="1a62e-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a62e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a62e-106">Syntax</span></span>

<span data-ttu-id="1a62e-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="1a62e-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="1a62e-108">*выражение* Выражение, возвращающее объект **поля** .</span><span class="sxs-lookup"><span data-stu-id="1a62e-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a62e-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a62e-109">Remarks</span></span>

<span data-ttu-id="1a62e-110">Параметры или возвращаемые значения — это строка, описывающая сравнения в виде SQL, ГДЕ предложения WHERE без зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="1a62e-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="1a62e-111">Для объекта еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1a62e-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="1a62e-112">**Значение** определяет, содержит ли поле допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="1a62e-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="1a62e-113">Если данные не является допустимым, возникает перехватываемые ошибки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a62e-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="1a62e-114">Сообщения об ошибке — текст свойства **[сообщение об ошибке](field-validationtext-property-dao.md)** , если указан или текст заданное **значение**.</span><span class="sxs-lookup"><span data-stu-id="1a62e-114">The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="1a62e-115">Для объекта **[поля](field-object-dao.md)** используйте **значение** зависит от объекта, который содержит коллекцию **полей** , к которому добавляется объект **поля** .</span><span class="sxs-lookup"><span data-stu-id="1a62e-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a62e-116">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="1a62e-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="1a62e-117">Применение</span><span class="sxs-lookup"><span data-stu-id="1a62e-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a62e-118"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="1a62e-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="1a62e-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a62e-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a62e-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="1a62e-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1a62e-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a62e-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a62e-122"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="1a62e-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="1a62e-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a62e-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a62e-124"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="1a62e-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="1a62e-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a62e-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a62e-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="1a62e-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1a62e-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a62e-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a62e-128">Проверка поддерживается только для баз данных, которые используют ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1a62e-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="1a62e-129">Строковое выражение, указанного идентификатором \*\*значение объекта **поля** \*\* можно обратиться только для этого **поля**.</span><span class="sxs-lookup"><span data-stu-id="1a62e-129">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="1a62e-130">Выражение не может ссылаться на пользовательские функции, статистические функции SQL и запросы.</span><span class="sxs-lookup"><span data-stu-id="1a62e-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="1a62e-131">Чтобы задать \*\*значение объекта **поля** \*\* при его **Проверка набора** свойство имеет значение **True**, выражение необходимо успешно проанализировать (с именем подразумеваемых операнда) и иметь значение **True**.</span><span class="sxs-lookup"><span data-stu-id="1a62e-131">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="1a62e-132">Если значение свойства его **Проверка набора** присвоено **значение False**, параметр **значение** свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1a62e-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1a62e-133">Если свойству присвоено значение объединяется с дробное значение строки и системных параметров укажите десятичных знаков пробел (например, strRule = «ЦЕНЫ &gt; " &amp; lngPrice и lngPrice = 125,50), возникнет ошибка при код пытается проверить все данные.</span><span class="sxs-lookup"><span data-stu-id="1a62e-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="1a62e-134">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и ядро СУБД Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="1a62e-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


