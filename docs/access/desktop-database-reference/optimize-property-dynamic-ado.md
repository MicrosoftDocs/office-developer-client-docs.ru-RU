---
title: Оптимизация динамического свойства (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bb7872514a828fdd97fb404f5366c35ff9a883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288254"
---
# <a name="optimize-dynamic-property-ado"></a><span data-ttu-id="56e02-102">Оптимизация динамического свойства (ADO)</span><span class="sxs-lookup"><span data-stu-id="56e02-102">Optimize dynamic property (ADO)</span></span>


<span data-ttu-id="56e02-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56e02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56e02-104">Указывает, следует ли создавать индекс для поля.</span><span class="sxs-lookup"><span data-stu-id="56e02-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="56e02-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="56e02-105">Settings and return values</span></span>

<span data-ttu-id="56e02-106">Задает или возвращает **boolean значение,** которое указывает, следует ли создать индекс.</span><span class="sxs-lookup"><span data-stu-id="56e02-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e02-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="56e02-107">Remarks</span></span>

<span data-ttu-id="56e02-108">Индекс может повысить производительность операций поиска или сортировки значений в [наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="56e02-108">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="56e02-109">Индекс является внутренним для ADO — вы не можете получить явный доступ или использовать его в приложении.</span><span class="sxs-lookup"><span data-stu-id="56e02-109">The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="56e02-110">Чтобы создать индекс для поля, установите для свойства **Optimize** свойство **True.**</span><span class="sxs-lookup"><span data-stu-id="56e02-110">To create an index on a field, set the **Optimize** property to **True**.</span></span> <span data-ttu-id="56e02-111">Чтобы удалить индекс, установите для этого свойства свойство **False.**</span><span class="sxs-lookup"><span data-stu-id="56e02-111">To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="56e02-112">**Оптимизация** — это динамическое свойство, [](properties-collection-ado.md) которое применится к коллекции свойств объекта [Field,](field-object-ado.md) когда свойству [CursorLocation](cursorlocation-property-ado.md) задано свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="56e02-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="56e02-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="56e02-113">**Usage**</span></span>

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
