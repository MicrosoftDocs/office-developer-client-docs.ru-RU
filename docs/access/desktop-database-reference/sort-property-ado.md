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
# <a name="sort-property-ado"></a><span data-ttu-id="108d1-102">Свойство Sort (ADO)</span><span class="sxs-lookup"><span data-stu-id="108d1-102">Sort property (ADO)</span></span>


<span data-ttu-id="108d1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="108d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="108d1-104">Указывает одно или несколько имен [](recordset-object-ado.md) полей, по которым отсортировали набор записей, и указывает, сортировать ли каждое поле по возрастанию или убыванию.</span><span class="sxs-lookup"><span data-stu-id="108d1-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="108d1-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="108d1-105">Settings and return values</span></span>

<span data-ttu-id="108d1-106">Задает или возвращает **строку,** которая указывает имена полей в **наборе записей,** по которому необходимо отсортировать.</span><span class="sxs-lookup"><span data-stu-id="108d1-106">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="108d1-107">Каждое имя отделяется запятой, за которым при желании следует пустое ключевое слово **ASC,** которое сортировать поле в порядке возрастания, или **DESC,** который сортировать поле в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="108d1-107">Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order.</span></span> <span data-ttu-id="108d1-108">По умолчанию, если ключевое слово не указано, поле сортироваться в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="108d1-108">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="108d1-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="108d1-109">Remarks</span></span>

<span data-ttu-id="108d1-110">Для этого свойства свойство [CursorLocation](cursorlocation-property-ado.md) должно иметь свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="108d1-110">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="108d1-111">Для каждого поля, указанного в свойстве **Sort,** будет создан временный индекс, если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="108d1-111">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="108d1-112">Операция сортировки эффективна, так как данные физически не переупорядочены, а просто доступны в порядке, указанном индексом.</span><span class="sxs-lookup"><span data-stu-id="108d1-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="108d1-113">При **установке для** свойства Sort пустой строки строки сбрасываются в исходный порядок и удаляются временные индексы.</span><span class="sxs-lookup"><span data-stu-id="108d1-113">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="108d1-114">Существующие индексы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="108d1-114">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="108d1-115">**Предположим, что набор записей** содержит три поля с именами *firstName,* *middleInitial* и *lastName.*</span><span class="sxs-lookup"><span data-stu-id="108d1-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="108d1-116">Установите для свойства **Sort** строку "lastName DESC, firstName ASC", которая упорядочение набора **записей** по фамилии в порядке убытия, а затем по имени в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="108d1-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="108d1-117">Средний инициал игнорируется.</span><span class="sxs-lookup"><span data-stu-id="108d1-117">The middle initial is ignored.</span></span>

<span data-ttu-id="108d1-118">Ни один из полей не может называться ASC или DESC, так как эти имена конфликтуют с ключевыми словами **ASC** и **DESC.**</span><span class="sxs-lookup"><span data-stu-id="108d1-118">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="108d1-119">Придайте полю с конфликтующий именем псевдоним с помощью ключевого слова **AS** в запросе, возвращаемом **набором записей.**</span><span class="sxs-lookup"><span data-stu-id="108d1-119">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

