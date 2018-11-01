---
title: Свойство Sort (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd515d2812ce453711c2b6519b1875250911d1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886608"
---
# <a name="sort-property-ado"></a><span data-ttu-id="b3ba8-102">Свойство Sort (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3ba8-102">Sort property (ADO)</span></span>


<span data-ttu-id="b3ba8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3ba8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3ba8-104">Указывает одно или несколько имен полей на которых сортироваться [записей](recordset-object-ado.md) и ли сортироваться в каждом поле в возрастающем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b3ba8-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b3ba8-105">Settings and return values</span></span>

<span data-ttu-id="b3ba8-106">Задает или возвращает **строковое** значение, указывающее, имена полей в наборе **записей** , по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-106">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="b3ba8-107">Имя каждого разделенных точкой с запятой и при необходимости следуют пустым и ключевых слов, **ASC**, с которым Сортировка поля в порядке возрастания или **DESC**, который выполняется сортировка поля в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-107">Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order.</span></span> <span data-ttu-id="b3ba8-108">По умолчанию если нет ключевых слов не указан, то это поле является сортироваться в восходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-108">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ba8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3ba8-109">Remarks</span></span>

<span data-ttu-id="b3ba8-110">Это свойство требует свойства [CursorLocation](cursorlocation-property-ado.md) должно быть задано для **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-110">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="b3ba8-111">Временный индекс создается для каждого поля, указанных в свойстве **сортировки** , если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-111">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="b3ba8-112">Операция сортировки эффективен, так как данные физически не изменяется, но просто осуществляется в порядке, указанном в индексе.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="b3ba8-113">Свойства **сортировки** пустую строку Сброс исходный порядок строк и удалите временные индексы.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-113">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="b3ba8-114">Существующие индексы не удаляются.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-114">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="b3ba8-115">Предположим, что **набор записей** содержит три поля с именами *firstName*, *middleInitial*и *Фамилия*.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="b3ba8-116">Задайте для свойства **сортировки** в строку «Фамилия DESC, firstName ASC», который будут отсортированы **записей** по фамилии в порядке убывания, а затем по имени в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="b3ba8-117">Инициалы игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-117">The middle initial is ignored.</span></span>

<span data-ttu-id="b3ba8-118">Поле не может быть с именем «ASC» или «DESC» конфликтовать с ключевыми словами **ASC** и **DESC**их имена.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-118">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="b3ba8-119">Задайте псевдоним поля с конфликтующими именами с помощью ключевого слова **AS** в запрос, возвращающий **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="b3ba8-119">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

