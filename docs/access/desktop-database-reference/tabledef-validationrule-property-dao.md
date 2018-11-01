---
title: TableDef.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cbcd456e2c3d64364a7c01ea71174999159f0aa4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881722"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="fe2a5-102">TableDef.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe2a5-102">TableDef.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="fe2a5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe2a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe2a5-104">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись **строки**.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe2a5-105">Syntax</span></span>

<span data-ttu-id="fe2a5-106">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="fe2a5-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="fe2a5-107">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="fe2a5-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe2a5-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe2a5-108">Remarks</span></span>

<span data-ttu-id="fe2a5-109">Параметров или возвращаемых значений — это **строка** , описывающая сравнения в виде SQL, ГДЕ предложения WHERE без зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="fe2a5-110">Для объекта еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="fe2a5-111">**Значение** определяет, содержит ли поле допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="fe2a5-112">Если данные не является допустимым, возникает перехватываемые ошибки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="fe2a5-113">Сообщения об ошибке — текст свойства **сообщение об ошибке** , если указан или текст заданное **значение**.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="fe2a5-114">Проверка поддерживается только для баз данных, которые используют ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="fe2a5-115">Строковое выражение, указанного идентификатором \*\*значение объекта **поля** \*\* можно обратиться только для этого **поля**.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-115">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="fe2a5-116">Выражение не может ссылаться на пользовательские функции, статистические функции SQL и запросы.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-116">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="fe2a5-117">Чтобы задать \*\*значение объекта **поля** \*\* при его **Проверка набора** свойство имеет значение **True**, выражение необходимо успешно проанализировать (с именем подразумеваемых операнда) и иметь значение **True**.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-117">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="fe2a5-118">Если значение свойства его **Проверка набора** присвоено **значение False**, параметр **значение** свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-118">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="fe2a5-119">\*\*Значение объекта **записей** или **TableDef** \*\* может ссылаться на несколько полей в этот объект.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-119">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="fe2a5-120">Было указано ранее в этом разделе для объекта **поля** ограничения.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-120">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="fe2a5-121">Для объекта **TableDef** на основании связанной таблицы **значение** наследует значения свойства **значение** базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-121">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table.</span></span> <span data-ttu-id="fe2a5-122">Если базовый базовая таблица не поддерживает проверки, значение этого свойства является строкой нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="fe2a5-122">If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="fe2a5-123">Если свойству присвоено значение объединяется с дробное значение строки и системных параметров укажите десятичных знаков пробел (например, strRule = «ЦЕНЫ &gt; " &amp; lngPrice и lngPrice = 125,50), возникнет ошибка при код пытается проверить все данные.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="fe2a5-124">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="fe2a5-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>


