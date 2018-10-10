---
title: Recordset.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a70dc412cbca420ca689fbd956e56d5bcdea556
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481406"
---
# <a name="recordsetvalidationrule-property-dao"></a><span data-ttu-id="93186-102">Recordset.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="93186-102">Recordset.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="93186-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="93186-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="93186-104">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись **строки**.</span><span class="sxs-lookup"><span data-stu-id="93186-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="93186-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93186-105">Syntax</span></span>

<span data-ttu-id="93186-106">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="93186-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="93186-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="93186-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="93186-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="93186-108">Remarks</span></span>

<span data-ttu-id="93186-109">Параметров или возвращаемых значений — это **строка** , описывающая сравнения в виде SQL, ГДЕ предложения WHERE без зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="93186-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="93186-110">Для объекта еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="93186-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="93186-111">**Значение** определяет, содержит ли поле допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="93186-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="93186-112">Если данные не является допустимым, возникает перехватываемые ошибки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="93186-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="93186-113">Сообщения об ошибке — текст свойства **сообщение об ошибке** , если указан или текст заданное **значение**.</span><span class="sxs-lookup"><span data-stu-id="93186-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="93186-114">Для объекта **набора записей** **значение** используется только для чтения.</span><span class="sxs-lookup"><span data-stu-id="93186-114">For a **Recordset** object, use of the **ValidationRule** property is read-only.</span></span> <span data-ttu-id="93186-115">Для объекта **TableDef** использование **значение** зависит от состояния объекта **TableDef** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="93186-115">For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93186-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="93186-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="93186-117">Применение</span><span class="sxs-lookup"><span data-stu-id="93186-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93186-118">Базовая таблица</span><span class="sxs-lookup"><span data-stu-id="93186-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="93186-119">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93186-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93186-120">Связанные таблицы</span><span class="sxs-lookup"><span data-stu-id="93186-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="93186-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="93186-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93186-122">Проверка поддерживается только для баз данных, которые используют ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="93186-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="93186-123">Строковое выражение, указанного идентификатором \*\*значение объекта **поля** \*\* можно обратиться только для этого **поля**.</span><span class="sxs-lookup"><span data-stu-id="93186-123">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="93186-124">Выражение не может ссылаться на пользовательские функции, статистические функции SQL и запросы.</span><span class="sxs-lookup"><span data-stu-id="93186-124">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="93186-125">Чтобы задать \*\*значение объекта **поля** \*\* при его **Проверка набора** свойство имеет значение **True**, выражение необходимо успешно проанализировать (с именем подразумеваемых операнда) и иметь значение **True**.</span><span class="sxs-lookup"><span data-stu-id="93186-125">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="93186-126">Если значение свойства его **Проверка набора** присвоено **значение False**, параметр **значение** свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="93186-126">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="93186-127">\*\*Значение объекта **записей** или **TableDef** \*\* может ссылаться на несколько полей в этот объект.</span><span class="sxs-lookup"><span data-stu-id="93186-127">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="93186-128">Было указано ранее в этом разделе для объекта **поля** ограничения.</span><span class="sxs-lookup"><span data-stu-id="93186-128">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="93186-129">Для объекта **набора записей** в таблице тип **значение** наследует **условие на значение** поля свойства объекта **TableDef** , которая используется для создания объекта **набора записей** в таблице тип.</span><span class="sxs-lookup"><span data-stu-id="93186-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="93186-130">Если свойству присвоено значение объединяется с дробное значение строки и системных параметров укажите десятичных знаков пробел (например, strRule = «ЦЕНЫ &gt; " &amp; lngPrice и lngPrice = 125,50), возникнет ошибка при код пытается проверить все данные.</span><span class="sxs-lookup"><span data-stu-id="93186-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="93186-131">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="93186-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>


