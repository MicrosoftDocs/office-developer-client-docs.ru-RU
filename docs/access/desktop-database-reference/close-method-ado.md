---
title: 'Метод Close: ActiveX Data Objects (ADO)'
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296313"
---
# <a name="close-method-ado"></a><span data-ttu-id="568e4-102">Метод Close (ADO)</span><span class="sxs-lookup"><span data-stu-id="568e4-102">Close method (ADO)</span></span>


<span data-ttu-id="568e4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="568e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="568e4-104">Закрывает открытый объект и все зависимые объекты.</span><span class="sxs-lookup"><span data-stu-id="568e4-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="568e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="568e4-105">Syntax</span></span>

<span data-ttu-id="568e4-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="568e4-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="568e4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="568e4-107">Remarks</span></span>

<span data-ttu-id="568e4-108">Используйте метод **Close** для закрытия [подключения](connection-object-ado.md), [записи](record-object-ado.md), [набора записей](recordset-object-ado.md)или объекта [Stream](stream-object-ado.md) , чтобы освободить все связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="568e4-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="568e4-109">При закрытии объекта его не удаляются из памяти; Вы можете изменить его свойства и открыть позже.</span><span class="sxs-lookup"><span data-stu-id="568e4-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="568e4-110">Чтобы полностью удалить объект из памяти, присвойте переменной объекта значение *Nothing* (в Visual Basic) после закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="568e4-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="568e4-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="568e4-111">**Connection**</span></span>

<span data-ttu-id="568e4-112">При закрытии объекта **Connection** с помощью метода **Close** также закрываются все активные объекты **Recordset** , связанные с подключением.</span><span class="sxs-lookup"><span data-stu-id="568e4-112">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection.</span></span> <span data-ttu-id="568e4-113">Объект [Command](command-object-ado.md) , связанный с закрываемым объектом **Connection** , будет оставаться несвязанным, но больше не будет связан с объектом **Connection** ; то есть для свойства [ActiveConnection](activeconnection-property-ado.md) будет задано значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="568e4-113">A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**.</span></span> <span data-ttu-id="568e4-114">Кроме того, коллекция [Parameters](parameters-collection-ado.md) объекта **Command** будет очищена от любых параметров, определенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="568e4-114">Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="568e4-115">Позже можно вызвать метод [Open](open-method-ado-connection.md) , чтобы повторно установить подключение к тому же или другому источнику данных.</span><span class="sxs-lookup"><span data-stu-id="568e4-115">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source.</span></span> <span data-ttu-id="568e4-116">Когда объект **Connection** закрывается, вызов всех методов, которым требуется открытое подключение к источнику данных, приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="568e4-116">While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="568e4-117">Закрытие объекта **Connection** при наличии открытых объектов **Recordset** в подключении выполняет откат всех ожидающих изменений во всех объектах **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="568e4-117">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects.</span></span> <span data-ttu-id="568e4-118">Явное закрытие объекта **Connection** (вызов метода **Close** ) во время выполнения транзакции приводит к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="568e4-118">Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error.</span></span> <span data-ttu-id="568e4-119">Если объект **Connection** выходит за пределы области действия в ходе выполнения транзакции, ADO автоматически выполняет откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="568e4-119">If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="568e4-120">**Recordset, Record, Stream**</span><span class="sxs-lookup"><span data-stu-id="568e4-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="568e4-121">При использовании метода **Close** для закрытия связанных данных **Recordset**, **Record**или **Stream** освобождается и любой монопольный доступ к данным с помощью этого конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="568e4-121">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object.</span></span> <span data-ttu-id="568e4-122">Позже можно вызвать метод [Open](open-method-ado-recordset.md) , чтобы повторно открыть объект с теми же или измененными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="568e4-122">You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="568e4-123">При закрытии объекта **Recordset** при вызове всех методов, требующих наличия Live курсора, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="568e4-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="568e4-124">Если редактирование выполняется в режиме немедленного обновления, вызов метода **Close** приводит к возникновению ошибки; Вместо этого сначала вызовите метод [Update](update-method-ado.md) или [CancelUpdate](cancelupdate-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="568e4-124">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span> <span data-ttu-id="568e4-125">Если объект **Recordset** закрывается в режиме пакетного обновления, все изменения, выполненные с момента последнего вызова [UpdateBatch](updatebatch-method-ado.md) , теряются.</span><span class="sxs-lookup"><span data-stu-id="568e4-125">If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="568e4-126">Если вы используете метод [clone](clone-method-ado.md) для создания копий объекта Open **Recordset** , закрытие исходного объекта или клона не повлияет на другие копии.</span><span class="sxs-lookup"><span data-stu-id="568e4-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

