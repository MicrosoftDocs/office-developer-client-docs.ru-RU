---
title: Свойство Source (записей ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32d3d44094e9e5922b7c5e0cfa59ccd1f344ef0f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879140"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="3a7a9-102">Свойство Source (записей ADO)</span><span class="sxs-lookup"><span data-stu-id="3a7a9-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="3a7a9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a7a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a7a9-104">Указывает источник данных для объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3a7a9-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3a7a9-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3a7a9-105">Settings and return values</span></span>

<span data-ttu-id="3a7a9-106">Задает **строковое** значение или ссылку на объект [Command](command-object-ado.md) ; Возвращает только **строковое** значение, указывающее источник **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="3a7a9-106">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a7a9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a7a9-107">Remarks</span></span>

<span data-ttu-id="3a7a9-108">Используйте свойство **Source** , чтобы указать источник данных для объекта **набора записей** с помощью одного из следующих действий: переменной объекта **команды** , инструкции SQL, хранимую процедуру или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a7a9-108">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="3a7a9-109">Если задать свойство **Source** для объекта **команды** , свойство [ActiveConnection](activeconnection-property-ado.md) объекта **набора записей** наследует значение свойства **ActiveConnection** для указанного объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="3a7a9-109">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object.</span></span> <span data-ttu-id="3a7a9-110">Тем не менее чтение свойство **Source** не возвращает объект **команды** ; Вместо этого он возвращает свойство [CommandText](commandtext-property-ado.md) объекта **команды** , к которому задать свойство **источника** .</span><span class="sxs-lookup"><span data-stu-id="3a7a9-110">However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="3a7a9-111">Если свойство **Source** инструкции SQL, хранимую процедуру или имя таблицы, можно оптимизировать производительность, передав соответствующий аргумент *параметров* с помощью вызова метода [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="3a7a9-111">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="3a7a9-112">Свойство **Source** — чтение и запись для закрытой объектов **наборов записей** и доступны только для чтения, для открытия объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3a7a9-112">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

