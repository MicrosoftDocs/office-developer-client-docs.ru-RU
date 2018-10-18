---
title: Optimize Property--Dynamic (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605179"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="33353-102">Optimize Property--Dynamic (ADO)</span><span class="sxs-lookup"><span data-stu-id="33353-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="33353-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="33353-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33353-104">Указывает, должен быть создан индекс для поля.</span><span class="sxs-lookup"><span data-stu-id="33353-104">Specifies whether an index should be created on a field.</span></span>

<span data-ttu-id="33353-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="33353-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="33353-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="33353-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="33353-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="33353-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="33353-108">master</span><span class="sxs-lookup"><span data-stu-id="33353-108">master</span></span>

<span data-ttu-id="33353-109">Задает или возвращает значение **типа Boolean** , которое указывает, должен быть создан индекс.</span><span class="sxs-lookup"><span data-stu-id="33353-109">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="33353-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="33353-110">Remarks</span></span>

<span data-ttu-id="33353-111">Индекс можно повысить производительность операций, поиск или отсортировать значения в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="33353-111">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="33353-112">Индекс является внутренним в ADO — явно не удается получить доступ к или использовать в приложении.</span><span class="sxs-lookup"><span data-stu-id="33353-112">The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="33353-113">Чтобы создать индекс для поля, присвойте свойству **оптимизировать** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="33353-113">To create an index on a field, set the **Optimize** property to **True**.</span></span> <span data-ttu-id="33353-114">Чтобы удалить индекс, этому свойству присвоено значение **False**.</span><span class="sxs-lookup"><span data-stu-id="33353-114">To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="33353-115">**Оптимизировать** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [поля](field-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="33353-115">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="33353-116">**Использование**</span><span class="sxs-lookup"><span data-stu-id="33353-116">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
