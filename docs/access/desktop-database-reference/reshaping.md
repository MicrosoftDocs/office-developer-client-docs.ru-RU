---
title: Изменения формы (доступа к рабочему столу ссылку на базу данных)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9e0f8e017e91152ed876b933e0c0c01a7f355e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483259"
---
# <a name="reshaping"></a><span data-ttu-id="99d47-102">Reshaping</span><span class="sxs-lookup"><span data-stu-id="99d47-102">Reshaping</span></span>


<span data-ttu-id="99d47-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99d47-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="99d47-104">**Записей** , созданные с помощью предложения команду фигуры может быть назначен в имя *псевдонима* (обычно с ключевым словом AS).</span><span class="sxs-lookup"><span data-stu-id="99d47-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="99d47-105">Псевдоним формы **записей** можно ссылаться в совершенно иной команды.</span><span class="sxs-lookup"><span data-stu-id="99d47-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="99d47-106">То есть, который может повторно использовать, или *Изменить форму*, ранее формы **записей** в новую команду фигуры.</span><span class="sxs-lookup"><span data-stu-id="99d47-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="99d47-107">Для поддержки этой функции, ADO предоставляет свойство, [Имя формы](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="99d47-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="99d47-108">Изменение формы имеет две основные функции.</span><span class="sxs-lookup"><span data-stu-id="99d47-108">Reshaping has two main functions.</span></span> <span data-ttu-id="99d47-109">Первый фильтр — Связывание существующих **записей** с новым родительским **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="99d47-109">The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="99d47-110">Пример</span><span class="sxs-lookup"><span data-stu-id="99d47-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="99d47-111">Вторая функция является возможность не разбитых доступ к существующим объектам дочерних **записей** , используя синтаксис `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="99d47-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>


> [!NOTE]
> <P><span data-ttu-id="99d47-112">Не удается добавить столбцы в существующих <STRONG>записей</STRONG>, изменить форму параметризованного <STRONG>набора записей</STRONG> или объектов <STRONG>наборов записей</STRONG> в любой промежуточных предложение COMPUTE или выполнение статистического операций в любого потомка <STRONG>записей</STRONG> из <STRONG> Набор записей</STRONG> изменение формы.</span><span class="sxs-lookup"><span data-stu-id="99d47-112">You cannot append columns to an existing <STRONG>Recordset</STRONG>, reshape a parameterized <STRONG>Recordset</STRONG> or the <STRONG>Recordset</STRONG> objects in any intervening COMPUTE clause, or perform aggregate operations on any <STRONG>Recordset</STRONG> descendant from the <STRONG>Recordset</STRONG> being reshaped.</span></span> <span data-ttu-id="99d47-113"><STRONG>Набор записей</STRONG> преобразованию и новая команда фигуры необходимо использовать то же <A href="connection-object-ado.md">подключение</A>.</span><span class="sxs-lookup"><span data-stu-id="99d47-113">The <STRONG>Recordset</STRONG> being reshaped and the new shape command must both use the same <A href="connection-object-ado.md">Connection</A>.</span></span></P>


