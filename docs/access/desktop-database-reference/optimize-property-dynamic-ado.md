---
title: Оптимизация динамической свойство (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a1fff5911080811bc2556a20667ff2f2391f22e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926782"
---
# <a name="optimize-dynamic-property-ado"></a><span data-ttu-id="f6a77-102">Оптимизация динамической свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6a77-102">Optimize dynamic property (ADO)</span></span>


<span data-ttu-id="f6a77-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6a77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6a77-104">Указывает, должен быть создан индекс для поля.</span><span class="sxs-lookup"><span data-stu-id="f6a77-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f6a77-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f6a77-105">Settings and return values</span></span>

<span data-ttu-id="f6a77-106">Задает или возвращает значение **типа Boolean** , которое указывает, должен быть создан индекс.</span><span class="sxs-lookup"><span data-stu-id="f6a77-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a77-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6a77-107">Remarks</span></span>

<span data-ttu-id="f6a77-108">Индекс можно повысить производительность операций, поиск или отсортировать значения в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f6a77-108">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="f6a77-109">Индекс является внутренним в ADO — явно не удается получить доступ к или использовать в приложении.</span><span class="sxs-lookup"><span data-stu-id="f6a77-109">The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="f6a77-110">Чтобы создать индекс для поля, присвойте свойству **оптимизировать** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="f6a77-110">To create an index on a field, set the **Optimize** property to **True**.</span></span> <span data-ttu-id="f6a77-111">Чтобы удалить индекс, этому свойству присвоено значение **False**.</span><span class="sxs-lookup"><span data-stu-id="f6a77-111">To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="f6a77-112">**Оптимизировать** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [поля](field-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="f6a77-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="f6a77-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="f6a77-113">**Usage**</span></span>

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
