---
title: Изменения формы (доступа к рабочему столу ссылку на базу данных)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49a61e72a4d9260b73275d84ce912ebc76f37652
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996456"
---
# <a name="reshaping"></a><span data-ttu-id="e4655-102">Изменение формы</span><span class="sxs-lookup"><span data-stu-id="e4655-102">Reshaping</span></span>

<span data-ttu-id="e4655-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4655-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4655-104">**Записей** , созданные с помощью предложения команду фигуры может быть назначен в имя *псевдонима* (обычно с ключевым словом AS).</span><span class="sxs-lookup"><span data-stu-id="e4655-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="e4655-105">Псевдоним формы **записей** можно ссылаться в совершенно иной команды.</span><span class="sxs-lookup"><span data-stu-id="e4655-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="e4655-106">То есть, который может повторно использовать, или *Изменить форму*, ранее формы **записей** в новую команду фигуры.</span><span class="sxs-lookup"><span data-stu-id="e4655-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="e4655-107">Для поддержки этой функции, ADO предоставляет свойство, [Имя формы](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e4655-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="e4655-108">Изменение формы имеет две основные функции.</span><span class="sxs-lookup"><span data-stu-id="e4655-108">Reshaping has two main functions.</span></span> <span data-ttu-id="e4655-109">Первый фильтр — Связывание существующих **записей** с новым родительским **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e4655-109">The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="e4655-110">Пример</span><span class="sxs-lookup"><span data-stu-id="e4655-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="e4655-111">Вторая функция является возможность не разбитых доступ к существующим объектам дочерних **записей** , используя синтаксис `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="e4655-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="e4655-112">Не удается добавить столбцы в существующих **записей**, изменить форму параметризованного **набора записей** или объектов **наборов записей** в любой промежуточных предложение COMPUTE или выполнение статистического операций в любого потомка **записей** из \*\* Набор записей\*\* изменение формы.</span><span class="sxs-lookup"><span data-stu-id="e4655-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="e4655-113">**Записей** преобразованию и его команды должны использовать же \*\* объект[подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e4655-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


