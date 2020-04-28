---
title: Свойство Sort (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 62ac60b1c7575f0b0d3e003dc58a11fe4d86c131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308640"
---
# <a name="sort-property-ado"></a><span data-ttu-id="8f320-102">Свойство Sort (ADO)</span><span class="sxs-lookup"><span data-stu-id="8f320-102">Sort property (ADO)</span></span>


<span data-ttu-id="8f320-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f320-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f320-104">Указывает одно или несколько имен полей, в которых сортируется [набор записей](recordset-object-ado.md) , и каждое поле сортируется в возрастающем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="8f320-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8f320-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8f320-105">Settings and return values</span></span>

<span data-ttu-id="8f320-106">Задает или возвращает **строковое** значение, которое указывает имена полей в **наборе записей** , по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="8f320-106">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="8f320-107">Каждое имя отделяется запятой и при необходимости следует указать пустое значение и ключевое слово **ASC**, которое сортирует поле в возрастающем порядке, или **DESC**, который сортирует поле по убыванию.</span><span class="sxs-lookup"><span data-stu-id="8f320-107">Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order.</span></span> <span data-ttu-id="8f320-108">По умолчанию при условии, что ключевое слово не задано, поле сортируется в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="8f320-108">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f320-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f320-109">Remarks</span></span>

<span data-ttu-id="8f320-110">Для этого свойства необходимо задать для свойства [CursorLocation](cursorlocation-property-ado.md) значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="8f320-110">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="8f320-111">Для каждого поля, указанного в свойстве **Sort** , будет создан временный индекс, если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="8f320-111">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="8f320-112">Операция сортировки эффективна, так как данные не переупорядочиваются физически, но доступ к ним осуществляется только в порядке, указанном индексом.</span><span class="sxs-lookup"><span data-stu-id="8f320-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="8f320-113">Если задать для свойства **Sort** пустую строку, строки будут сброшены в исходный порядок и удалять временные индексы.</span><span class="sxs-lookup"><span data-stu-id="8f320-113">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="8f320-114">Существующие индексы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="8f320-114">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="8f320-115">Предположим, что объект **Recordset** содержит три поля с именами *FirstName*, *миддлеинитиал*и *LastName*.</span><span class="sxs-lookup"><span data-stu-id="8f320-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="8f320-116">Задайте для свойства **Sort** строку "LastName DESC, FirstName ASC", которая будет упорядочивать **набор записей** по фамилии в убывающем порядке, а затем по имени по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="8f320-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="8f320-117">Посрединный инициал игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8f320-117">The middle initial is ignored.</span></span>

<span data-ttu-id="8f320-118">Поле не может называться "ASC" или "DESC", так как эти имена конфликтуют с ключевыми словами **ASC** и **DESC**.</span><span class="sxs-lookup"><span data-stu-id="8f320-118">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="8f320-119">Присвойте полю с конфликтующим именем псевдоним, используя ключевое слово **as** в запросе, возвращающем **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="8f320-119">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

