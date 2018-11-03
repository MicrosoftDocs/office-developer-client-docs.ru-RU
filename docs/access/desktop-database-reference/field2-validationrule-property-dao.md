---
title: Свойство Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 354b080b40c9dfc59394f1a860453e539c5949fb
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936604"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="0d2a8-102">Свойство Field2.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d2a8-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="0d2a8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d2a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d2a8-104">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0d2a8-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0d2a8-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2a8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d2a8-106">Syntax</span></span>

<span data-ttu-id="0d2a8-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="0d2a8-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="0d2a8-108">*выражение* Выражение, возвращающее объект **поле2** .</span><span class="sxs-lookup"><span data-stu-id="0d2a8-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d2a8-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d2a8-109">Remarks</span></span>

<span data-ttu-id="0d2a8-110">Параметры или возвращаемые значения — это строка, описывающая сравнения в виде SQL, ГДЕ предложения WHERE без зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="0d2a8-111">Для объекта еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="0d2a8-112">**Значение** определяет, содержит ли поле допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="0d2a8-113">Если данные не является допустимым, возникает перехватываемые ошибки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="0d2a8-114">Сообщения об ошибке — текст свойства **сообщение об ошибке** , если указан или текст заданное **значение**.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-114">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="0d2a8-115">Для объекта **поле2** использование **значение** зависит от объекта, которое содержит коллекцию **полей** , к которому добавляется объект **поле2** .</span><span class="sxs-lookup"><span data-stu-id="0d2a8-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d2a8-116">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="0d2a8-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="0d2a8-117">Применение</span><span class="sxs-lookup"><span data-stu-id="0d2a8-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d2a8-118"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="0d2a8-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2a8-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0d2a8-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d2a8-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0d2a8-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2a8-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2a8-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d2a8-122"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="0d2a8-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2a8-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2a8-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d2a8-124"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="0d2a8-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2a8-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0d2a8-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d2a8-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0d2a8-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2a8-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d2a8-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d2a8-128">Проверка поддерживается только для баз данных, которые используют ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="0d2a8-129">Строковое выражение, заданное свойством **значение** объекта **поле2** можно обратиться только к этой **поле2**.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-129">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**.</span></span> <span data-ttu-id="0d2a8-130">Выражение не может ссылаться на пользовательские функции, статистические функции SQL и запросы.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="0d2a8-131">Чтобы задать \*\*значение объекта **поле2** \*\* при его **Проверка набора** свойство имеет значение **True**, выражение успешно необходимо проанализировать (с именем подразумеваемых операнда) и значение **True**.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-131">To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="0d2a8-132">Если значение свойства его **Проверка набора** присвоено **значение False**, параметр **значение** свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="0d2a8-133">Если свойству присвоено значение объединяется с дробное значение строки и системных параметров укажите десятичных знаков пробел (например, strRule = «ЦЕНЫ &gt; " &amp; lngPrice и lngPrice = 125,50), возникнет ошибка при код пытается проверить все данные.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="0d2a8-134">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и ядро СУБД Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="0d2a8-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


