---
title: Свойство Source (Recordset в ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306414"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="82899-102">Свойство Source (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="82899-102">Source property (ADO Recordset)</span></span>


<span data-ttu-id="82899-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82899-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82899-104">Указывает источник данных для объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82899-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="82899-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="82899-105">Settings and return values</span></span>

<span data-ttu-id="82899-106">Задает **ссылку на объект String** или [Command;](command-object-ado.md) возвращает только **значение String,** которое указывает источник **recordset.**</span><span class="sxs-lookup"><span data-stu-id="82899-106">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="82899-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="82899-107">Remarks</span></span>

<span data-ttu-id="82899-108">Используйте свойство **Source** для указания источника данных для объекта **Recordset**  с помощью одного из следующих объектов: переменной объекта Command, SQL, сохраненной процедуры или имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="82899-108">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="82899-109">Если задано свойство **Source** для объекта **Command,** свойство [ActiveConnection](activeconnection-property-ado.md) объекта **Recordset** наследует значение свойства **ActiveConnection** для указанного объекта **Command.**</span><span class="sxs-lookup"><span data-stu-id="82899-109">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object.</span></span> <span data-ttu-id="82899-110">Однако чтение свойства **Source** не возвращает объект **Command;** вместо этого возвращается свойство [CommandText](commandtext-property-ado.md) объекта **Command,** к которому вы установите **свойство Source.**</span><span class="sxs-lookup"><span data-stu-id="82899-110">However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="82899-111">Если свойство **Source** — это SQL, сохраненная процедура или имя таблицы, вы можете оптимизировать производительность, передав соответствующий аргумент *Параметры* вызовом [метода Open.](open-method-ado-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="82899-111">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="82899-112">Свойство **Source** является объектом чтения и записи для закрытых объектов **Recordset** и только для объектов open **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="82899-112">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

