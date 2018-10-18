---
title: Source Property (ADO Recordset)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605263"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="5d376-102">Source Property (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="5d376-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="5d376-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d376-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d376-104">Указывает источник данных для объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5d376-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="5d376-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5d376-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="5d376-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5d376-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="5d376-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5d376-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="5d376-108">master</span><span class="sxs-lookup"><span data-stu-id="5d376-108">master</span></span>

<span data-ttu-id="5d376-109">Задает **строковое** значение или ссылку на объект [Command](command-object-ado.md) ; Возвращает только **строковое** значение, указывающее источник **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5d376-109">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d376-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="5d376-110">Remarks</span></span>

<span data-ttu-id="5d376-111">Используйте свойство **Source** , чтобы указать источник данных для объекта **набора записей** с помощью одного из следующих действий: переменной объекта **команды** , инструкции SQL, хранимую процедуру или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d376-111">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="5d376-112">Если задать свойство **Source** для объекта **команды** , свойство [ActiveConnection](activeconnection-property-ado.md) объекта **набора записей** наследует значение свойства **ActiveConnection** для указанного объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="5d376-112">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object.</span></span> <span data-ttu-id="5d376-113">Тем не менее чтение свойство **Source** не возвращает объект **команды** ; Вместо этого он возвращает свойство [CommandText](commandtext-property-ado.md) объекта **команды** , к которому задать свойство **источника** .</span><span class="sxs-lookup"><span data-stu-id="5d376-113">However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="5d376-114">Если свойство **Source** инструкции SQL, хранимую процедуру или имя таблицы, можно оптимизировать производительность, передав соответствующий аргумент *параметров* с помощью вызова метода [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="5d376-114">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="5d376-115">Свойство **Source** — чтение и запись для закрытой объектов **наборов записей** и доступны только для чтения, для открытия объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5d376-115">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

